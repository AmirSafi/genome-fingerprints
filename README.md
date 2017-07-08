# genome-fingerprints
Software for creating and comparing genome fingerprints.  
More information and datasets: http://db.systemsbiology.net/gestalt/genome_fingerprints/

1. To create a fingerprint for a genome:  
	bin/computeDMF.pl myGenome path-to-my-vcfs/myGenome.vcf.gz  
	...will generate myGenome.outn.gz (and some other files)

2. To compare two fingerprints:  
	bin/compareDMFs.pl myFirstGenome.outn.gz mySecondGenome.outn.gz

3. To serialize fingerprints into a database, using L=120:  
	bin/serializeDMFs.pl myFingerprintCollection 120 @myListOfFingerprints  
	bin/serializeDMFs.pl myFingerprintCollection 120 *.outn.gz

4. To compare a fingerprint to a database:  
	bin/searchDMFs.pl myFirstGenome.outn.gz myFingerprintCollection  
	...see the data directory for an example database (CEPH1463 pedigree)

5. To compare two databases:  
	bin/searchDMFs.pl aFingerprintCollection anotherFingerprintCollection

6. To perform all-against-all comparisons in one database:  
	bin/searchDMFs.pl aFingerprintCollection


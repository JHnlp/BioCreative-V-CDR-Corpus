BioCreative V - Chemical-disease relation (CDR) task corpus release

Task information:
	Automatic detection of chemical/drugs and diseases, and their relations in PubMed abstracts. In particular, the CDR task focuses on extracting the relationship of drug-induced diseases. 

Organizers:
	Zhiyong Lu, NCBI (zhiyong.lu@nih.gov)
	Thomas Wiegers, North Carolina State University (tcwieger@ncsu.edu )
	
Files:
	CDR_sample.txt : Sample Set (50 articles) in PubTator format
	CDR_sample.xml : Sample Set (50 articles) in BioC format
	BioC.dtd : The DTD file describes the structure of an XML file, additional information, such as the data semantics, must be known before the data in the XML file can be effectively used.
	BC5CDR.key: BioC XML file. The key file allows the creator to specify details of how the data in the XML file should be interpreted.
	
Format:
	BioC : It's a sample format to share text data and annotations. You can find sample code (e.g., C++, Java, Perl and Python) in http://bioc.sourceforge.net/ to parse information of BioC file.
	
	PubTator : PubTator (http://www.ncbi.nlm.nih.gov/CBBresearch/Lu/Demo/PubTator/) is a web-based tool for accelerating manual literature curation through the use of advanced text-mining techniques.
		The first row is title, and second row is abstract. The rows below abstract are bioconcept mentions. Between any two articles, a blank line is required. We use six attributes to describe an 
		annotation, separated by Tab keys. The six attributes are: 
			
			PMID<tab>START OFFSET<tab>END OFFSET<tab>text MENTION<tab>mention TYPE (e.g. Disease)<tab>database IDENTIFIER<tab>Individual mentions
	
		Note that the last attribute "Individual mentions" is optional. It is only annotated once the MENTION is a composite mention. The START OFFSET is the first character offset of the mention while 
		END OFFSET is the last. 
		
		Example:
		
			3403780|t|Paracetamol-associated coma, metabolic acidosis, renal and hepatic failure.
			3403780|a|A case of metabolic acidosis, acute renal failure and hepatic failure following paracetamol ingestion is presented. The diagnostic difficulty at presentation is highlighted .....
			3403780	0	11	Paracetamol	Chemical	D000082	
			3403780	23	27	coma	Disease	D003128	
			3403780	29	47	metabolic acidosis	Disease	D000138	
			3403780	39	47	acidosis	Disease	D000138	
			3403780	49	74	renal and hepatic failure	Disease	D058186|D017093	renal failure|hepatic failure
			3403780	86	104	metabolic acidosis	Disease	D000138	
			3403780	96	104	acidosis	Disease	D000138	
			3403780	106	145	acute renal failure and hepatic failure	Disease	D058186|D017114	acute renal failure|acute hepatic failure
			3403780	156	167	paracetamol	Chemical	D000082	
			3403780	CID	D000082	D000138
			3403780	CID	D000082	D017114
			3403780	CID	D000082	D058186
---# Chapter 4 - Metadata for Social Science Datasets> Metadata for Administrative and Social Science DataRobert B Allen\[0000-0002-4059-2587\]rba\@boballen.infoData are valuable but finding the right data is often difficult. Thischapter reviews current approaches and issues for metadata about numericdata and data sets that may facilitate the identification of relevantdata. In addition, the chapter reviews how metadata supportrepositories, portals, and services. There are emerging metadatastandards but they are applied unevenly so that there is nocomprehensive approach. There has been greater emphasis on structuralissues than on semantic descriptions.INTRODUCTION============Evidence-based policy needs relevant data (Commission on Evidence-BasedPolicy, 2018; Lane, 2016). Such data is valuable, but often difficult tofind and/or replicate. The FAIR Open Access guidelines suggest that,ideally, data should be Findable, Accessible, Interoperable, andReusable.[^1] Therefore, data curation and stewardship is needed.While data may include text, image, or video, here we focus on numericobservations recorded and maintained in machine-readable form. There aremany data sets of such observations available online; the DataCite[^2]repository alone contains over five million. There are many differenttypes of data sets. Data sets differ in their structure, their source,and their use. In some cases, they are single vectors of data; in othercases, they comprise all the data associated with one study or across agroup of related data sets. Following the approach of W3C-DCAT (WorldWide Web Consortium-Data Catalog Vocabulary)[^3], a data set may be acollection of related observations which is developed and managed by asingle entity such as a statistical agency. When stored as a unitonline, the data set is a digital object.Metadata consists of short descriptors which refer to a digital object.Metadata can support users in finding data sets, and enable users toknow what is in them. However, there is tremendous variability in thetypes of metadata and how they are applied. One categorization ofmetadata identifies structural (or technical), administrative, anddescriptive metadata. Structural metadata includes the organization ofthe files. Administrative metadata describes the permissions, rights,and usage. Descriptive metadata covers the contents.This chapter surveys the state of the art of metadata for numeric datasets, focusing on metadata for administrative and social sciencerecords. Administrative records describe details about the state of theworld as collected by organizations or agencies. They includegovernmental records, hospital records, educational records, andbusiness records. By comparison, social science data generally iscollected for the purpose of developing or applying theory.Section 2 describes data, metadata, and digital objects. Section 3discusses semantics. Section 4 considers repositories. Section 5describes services. Section 6 describes the techniques for documentingthe internal structure of data sets. Section 7 discussescyberinfrastructure.DATA, METADATA, AND DIGITAL DATA OBJECTS========================================A metadata element describes some attribute of a digital object. Thesimplest metadata identifies the digital object.[^4] Individual metadataelements are generally part of a set which describes attributes of adata set. Such a set of metadata elements can be structured as acatalog, schema, or frame, and restrictions can be placed on the valuesallowed for the individual elements. A fragment of an example of theSchema.org[^5] dataset schema is shown in Figure 1. Note the distinctmetadata elements in that fragment.Figure 1: Fragment of schema.org dataset schema[^6].The W3C DCAT[^7] is a schema standard for data sets that is used by manyrepositories such as data.gov. Other structured frameworks for data setsinclude the DataCite[^8] metadata schema and the Inter-universityConsortium for Political and Social Research Data DocumentationInitiative (ICPSR DDI) discussed below (Section 4.1). The catalogspecifications provide a flexible framework. For instance, DCAT allowsthe inclusion of metadata elements drawn from domain schema andontologies. Some of these domain schemas are widely used resources whichDCAT refers to as assets. For instance, spatial relationships are oftenmodeled by the Federal Geographic Data Committee (FGDC) standard.[^9]Many of the implementations for indexing collections of metadata schemasuse relational databases. Thus, they use SQL and support tools such asdata dictionaries. Moreover, they are often characterized by UnifiedModeling Language (UML) Class Diagrams which are common for datamodeling.SEMANTIC DESCRIPTIONS=====================Semantic data models have become widely explored. In particular, theSemantic Web utilizes nodes which are implemented with XML. RDF(Resource Description Framework) extends XML by requiring triples whichassert a relationship (property) between two identifiers:"identifier"-"property"-"identifier". By connecting triples, RDF candefine a graph network of the relationships among a set of controlledvocabulary terms; this is the essence of linked data.RDFS (RDF Schema) extends RDF by supporting class/subclassrelationships. The classes allowed for identifiers in RDFS triples arecontrolled by domain and range parameters. Traditional thesauri have asimple hierarchical structure, the Simple Knowledge Organization System(SKOS) is an RDFS standard for a machine-processable representation ofthesauri. Many administrative and social-science-related thesauri suchas EDGAR, and those of the World Bank, and the OECD have now beenimplemented with SKOS. In addition, a knowledge graph is a model of adomain, sometimes including instances, which may be implemented in SKOS.For example, DBpedia[^10] is a knowledge graph based on Wikipedia.Some frameworks for structural descriptions of data sets include aspectsof ontologies. For example, less formal ontologies simply providedefinitions and employ RDFS. Similarly, Schema.org schemas can be usedwith micro-formats which match schema elements with passages in anonline text. Schema.org has a classification of topics and mayincorporate other systems such as FOAF (Friend of a Friend) whichincludes attributes associated with people. Formal ontologies use OWL(Web Ontology Language) to add features to RDFS. These features lendthemselves to logical inference provided that the entities andrelationships are rigorously defined.Upper ontologies provide top-down structures for the types of entitiesallowed in derivative domain and application ontologies. One of the bestknown upper ontologies is the Basic Formal Ontology (BFO) (Arp, Smith, &Spear, 2015), which is a realist, Aristotelian approach. At thetop-level, BFO distinguishes between Continuants (endurants) andOccurrents (perdurants) and also between Universals and Particulars(instances). Many biological ontologies have been developed based on BFOand are collected in the Open Biomedical Ontology (OBO) Foundry.There are fewer rich ontologies dealing with social science content thanthere are for natural science. One challenge is "social ontology", thatis, developing definitions for social terms. It is difficult to defineexactly what is a family, a crime, or money. In most cases, anoperational definition or an approximate definition may suffice wherestructured documentation of the definitions are unavailable. Moreover,while social terms are especially difficult to define for vernacularspeech, it seems possible to make clear, though perhaps cumbersome,definitions for scholarly applications.DATA REPOSITORIES=================A data repository holds data sets and related digital objects. Itprovides access to the data sets and supports search. Metadata isintegral to these services at several levels. In addition to item-levelmetadata for the data sets, there can also be study-level metadata orcollection-level metadata.The Inter-University Consortium for Political and Social Research (ICPSR)-------------------------------------------------------------------------ICPSR[^11] is a major repository of public-use social science andadministrative data sets derived from questionnaires and surveys. TheICPSR DDI[^12] (e.g., Vardigan, Heus, & Thomas, 2009) defines a catalogcode. A notable feature is a codebook which saves the exact wording ofall the questions. In addition, the ICPSR provides an index of allvariable names that are used in the data sets. DDI-Lifecycle is anextension of DDI that describes the broader context in which the surveywas administered as well as the details about the preservation of thefile (see Section 5.3).Repositories of Governmental and NGO Statistical Agencies---------------------------------------------------------Statistical data collection is a core function of government. Mostcountries have national statistical agencies. While these statisticalcollections often emphasize social data, they also include relatedindicators such as agricultural and industrial output and housing, suchas Statistics New Zealand, and the Korean Social Science Data Archive(KOSSDA). European data sets are maintained in the Consortium ofEuropean Social Science Data Archives (CESSDA)[^13] and the EuropeanSocial Survey.[^14] Australia has a broad data management initiative,ANDS.[^15] Many U.S. governmental data sets are collected atdata.gov.[^16] In addition, there are many non-governmental andinter-governmental agencies such as the OECD, the World Bank, and theUnited Nations, which host data sets.Other Data Repositories-----------------------Many data sets are produced, curated, and used in the natural sciencessuch as astronomy and geosciences. Some of these data sets have highlyautomated data collection, elaborate archives and established curationmethods. Many of these repositories include multiple data sets for whichaccess is supported with portals or data cubes (see Section 6.1). Forinstance, massive amounts of geophysical data and related text documentsare collected in the EarthCube[^17] portal. The Science.gov portal isestablished by the U.S. Office of Science Technology and Policy. NASAsupports approximately 25 different data portals. Each satellite in theEarth Observation System (EOS) may provide hundreds of streams ofdata,[^18] with much common metadata. This provides a context analogousto study-level metadata. Likewise, there are massive genomics andproteomics data sets which are accessible via portals such asUniProt[^19] and the Protein Data Bank[^20] along with suites of toolsfor exploring them. Similarly, there are very large data sets frommedical research such as from clinical trials and from clinical practiceincluding Electronic Health Records (EHRs).Ecosystem of Texts and Data Sets--------------------------------Data sets are often associated with text reports. For example, the DryadDigital Repository[^21] hosts data sets from scholarly publicationswhich require the deposit of data associated with scholarly papersaccepted for publication. In addition, data sets may be cited in muchthe same way that research reports are cited. Formal citationfacilitates tracing the origins of data used in analyses and helps toacknowledge the work of the creators of the data sets. Standards havebeen developed for such citations (Martone, 2014; Silvello, 2017).SERVICES========The purpose of metadata and other aspects of information organizationand management is to provide services to users. Indeed, "servicescience" is an approach in information technology which focuses on thedesign and delivery of services rather than on underlying technologies.Search------Searching for data sets differs from the familiar web-based text searchbecause data repositories are generally hosted by either relationaldatabases or semantic triplestores. Even where the data are stored onseparate servers the metadata can be harvested and searched. This typeof federated search is supported by the Open Archives InitiativeProtocol for Metadata Harvesting (OAI-PMH);[^22] both data.gov and ICPSRuse OAI-PMH.From Statistical Packages to Virtual Research Environments----------------------------------------------------------There is an increasingly rich set of analytic tools. Some of theearliest tools were statistical packages such as SPSS, R, SAS, andSTATA. These were gradually enhanced with data visualization and otheranalytic software. The current generation of tools such as Jupyter,RSpace, and eLab notebooks (ELN) integrate annotations, workflows, rawdata, and data analysis into one platform. In addition, somerepositories have developed their own powerful data exploration toolssuch as ICPSR Colectica[^23] for DDI and the GSS Data Explorer[^24].Virtual research environments (VREs) are typically organized by researchcommunities to coordinate data sets with search and analytic tools. Forinstance, the Virtual Astronomy Observation (VAO) uses Jupyter toprovide users with a robust research environment. WissKI[^25] is aplatform for coordinating digital humanities data sets which are basedon Drupal.Preservation------------Lost data is often irreplaceable. Even if the data is not entirely lost,users need confidence that the quality of stored data has not beencompromised. Moreover, although data storage prices are decliningdramatically, we cannot save everything and the cost of maintaining atrusted repository remains substantial. Many of these challenges arefamiliar from traditional archives. For instance, selection policiestypical in archives could help in controlling the many poorly documenteddata sets in some repositories. Yet, prioritization is difficult[^26](Whyte & Wilson, 2010).The Open Archival Information System (OAIS) provides a reference modelfor the management of archives (Lee, 2010). The OAIS framework has beenincorporated into the ICPSR DDI-Lifecycle model. The IntegratedRule-Oriented Data System (iRODS)[^27] is a policy-based archivalmanagement system developed for large data stores. It implements aservice-oriented architecture (SOA) to support best practicesestablished by archivists.Provenance records the history of an entity. This can help to ensureconfidence in its authenticity. For data in a repository, provenanceoften means tracing the history of repository operations. The history oftransitions is often recorded as event data, where the events are whathappened to the data in the dataset. Typically, provenance ontologiesinclude actors, events, and digital objects. Potentially, blockchainscould provide an even greater level of trust in digital provenance.Metadata Quality and Metadata Management----------------------------------------Metadata, whether for texts or data sets, needs to be complete,consistent, standardized, machine processable, and timely (Park, 2009).A metadata editor supports the assignment of quality metadata (e.g.,Gonclaves, O'Conner, et al., 2019). When collections or metadatastandards change, the repository librarian must revise metadata (Tonkin,2009). This might be particularly needed when updating metadata fromdata streams[^28] such as those from satellite downlinks or smart-citysensors.Although survey results are generally aggregated across individuals,individual-level data is sometimes very useful. Some repositories ofsurvey data include micro-data, data for the responses that individualsgave to survey questions.[^29] Currently, there are no distinct metadatatags for such data; they are embedded into repository data. Moreover,the individual level of analysis raises privacy concerns and needs to becarefully managed; at the least, access should be limited to qualifiedresearchers.Metadata registries, such as the Marine Metadata InteroperabilityOntology Registry and Repository,[^30] record usage. The Registry ofResearch Data Repositories (re3data registry),[^31] which is operated byDataCite, links to more than 2000 different repositories each of whichholds many data sets. Each of the repositories is described by there3data.org schema for the description of research data repositories(Rücknagel, Vierkant, et al., 2015).Metadata application profiles provide constraints on the types ofentities that can be included in the metadata for a given application.For instance, DCAT Application Profiles (DCAT-AP) support standardizedmetadata exchange between repositories in different jurisdictions in theEU.[^32]DETAILS ABOUT THE DATA IN DATA SETS===================================Data Cubes----------Many notable data management techniques were originally developed formanaging and processing business data.[^33] One such technique is datacubes, which support access to multidimensional data. They present dataas if it filled cells of a high-dimensional cube, even if the data willprobably not fill all of the cells. Users can generate different viewsof the data by drilling-down, rolling-up, and slicing-and-dicing acrosscells. For complex data sets, there will be many dimensions. Tofacilitate retrieval, there can be a rich pre-coordinated index forcommon queries; other queries can be implemented with slower methodssuch as hashing or B-trees.Data cubes have been extended beyond business information processing tocubes such as the Statistical Data and Metadata eXchange (*SDMX) used inthe financial services industry and the* W3C Data Cube[^34] standardthat is applied in projects such as EarthCube.Sequential Activities and Modeling Research-------------------------------------------Entities change over time, yet knowledge representation frameworksrarely model change. In order to represent changes, models need torepresent transitions, processes, and other sequential activities. Suchmodeling is closer to the Unified Modeling Language (UML) or evenprogramming languages than to ontologies. In fact, modeling change isroutine for state machines, Petri nets, and other transition models. A"model-layer" that allows general statements to be made about sequentialactivities could incorporate both ontology and transitionals (Allen &Kim, 2018).Models of sequential activities include workflows and mechanisms (e.g.,Allen, 2018). A workflow is a structure for managing a sequence ofactivities and is a natural fit for describing research methods andanalyses (Austin, Bloom, et al., 2017). The Taverna workflow tool hasbeen widely used in the MyExperiment[^35] project, which provides aframework for capturing and posting research methods and incorporatesontologies such as FOAF.Allen (2015, 2018) has proposed direct representation of entire researchreports. This approach uses a programming language that blends upperontologies with object-oriented programming to do semantic modeling.Beyond modeling events, it is also possible to use structuredargumentation and assertions in scientific research reports.Potentially, social mechanisms (e.g., Hedstrom & Ylikoski, 2010) andcommunity models could be implemented. Further, highly-structuredevidence and claims might be applied to the evaluation of evidence-basedsocial policy.CYBERINFRASTRUCTURE===================Information Institutions and Organizations------------------------------------------Libraries and archives (whether traditional or digital) have themission, and often the resources, to develop standards and maintaininformation over the long-term. As noted earlier (Section 5.3),preservation is the fundamental concern for archival collections.Information institutions often have formal collection managementstrategies, metrics, and policies. These include Web and repositorymetrics and analytics, usage statistics such as reports of how manydownloads were made from data sets, and procedures for updates andformatting standards.In addition to traditional information institutions, there are now manyother players. These new players have slightly different mandates. Forexample, Schema.org's primary mission is to provide a structure thatimproves indexing by search engine companies. Nonetheless, theseorganizations often adopt best practices similar to those of traditionalinformation organizations.CrossRef[^36] and DataCite are DOI registration agencies. CrossRef is aportal to metadata for scholarly articles, while DataCite providesmetadata for digital objects associated with research. Increasingly, thetwo projects are coordinating. ORCID iDs[^37] are persistent digitalidentifiers assigned to authors. The emergence of structured identifierssuch as DOIs and ORCID iDs has allowed the development of services suchas VIVO[^38] and the Microsoft Academic Graph (MAG)[^39] which allowauthors to be tracked across research reports and projects, and acrosspublishers.Cloud Technologies, Software as a Service, and the Internet of Things---------------------------------------------------------------------We are now well into the era of cloud computing (Foster & Gannon, 2017),allowing flexible allocation of computing, networking and storageresources, which facilitates Software as a Service (SaaS). Thecompatibility of the versions of software packages needed for datamanagement is often a challenge. Containers, such as those from Docker,allow compatible versions of software to be assembled and run on avirtual computer. A container could hold datasets, workflows, and theprograms used to analyze the data, making the analyses readilyreplicable. Highly-networked data centers also facilitate the Internetof Things (IoT) which will generate massive data sets such as for "smartcities".CONCLUSION==========Data may not be useful when stand-alone without context. Some of thebiggest issues for the retrieval of information from data sets concerninformation organization, which help provide context. Metadata supportsthe discovery of and access to data sets. We need richer, moresystematic, and more interoperable metadata standards. Even moreattention to metadata would further support evidence-based policy.ACKNOWLEDGMENTS {#acknowledgments .ListParagraph}===============Julia Lane and members of NYU's Center for Urban Science and Progressprovided useful advice and comments.REFERENCES {#references .ListParagraph}==========Allen, R.B. (2015). Repositories with direct representation, *NetworkedKnowledge Representation Systems,* arXiv: 1512.09070Allen, R.B. (2018). *Issues for Using Semantic Modeling to RepresentMechanisms*, arXiv:1812.11431Allen, R.B., & Kim, YH. (2017/2018). Semantic Modeling with Foundries,arXiv:1801.00725Arp, R., Smith, B., & Spear, A.D. (2015). *Building Ontologies withBasic Formal Ontology*, MIT Press, Cambridge. MA.Austin, C.C., Bloom, T., Dallmeier-Tiessen, S., Khodiyar, V.K., Murphy,F., Nurnberger, A., et al. (2017). Key components of data publishing:Using current best practices to develop a reference model for datapublishing. *In[ternational Journal on DigitalLibraries](https://link.springer.com/journal/799), 18*(2) 77--92, doi:10.1007/s00799-016-0178-2Commission on Evidence-Based Policymaking. (2018). The Promise ofEvidence-Based Policymaking, <https://www.cep.gov/cep-final-report.html>Foster, I., & Gannon, D.B. (2017). Cloud Computing for Science andEngineering, MIT Press, Cambridge, MA.Gonçalves, R.S., O\'Connor, M.J., Martínez-Romero, M., Egyedi, A.L.,Willrett, D., Graybeal, J., & Musen, M.A. (2019). *The CEDAR workbench:an ontology-assisted environment for authoring metadata that describescientific experiments*. arXiv: 1905.06480Hedström, P., & Ylikoski, P. (2010). Causal mechanisms in the socialsciences. *Annual Review of Sociology*, *36* 49-67.Lane, J. (2016). Big data for public policy: The quadruple helix,*Journal Policy Analysis and Management, 35*(3), doi:[**10.1002/pam.21921**](https://doi.org/10.1002/pam.21921)Lee, C.A. (2010). Open Archival Information System (OAIS) ReferenceModel. *Encyclopedia of Library and Information Sciences* (3^rd^Edition). CRC Press, doi: 10.1081/E-ELIS3-120044377Martone M. (ed.) (2014). *Joint Declaration of Data CitationPrinciples*. San Diego CA: FORCE11, Data Citation Synthesis Group:<https://www.force11.org/group/joint-declaration-data-citation-principles-final>Park, JR., Metadata quality in digital repositories: A survey of thecurrent state of the art. *Cataloging & Classification Quarterly, 47*,213--228, 2009, doi: 10.1080/01639370902737240Rücknagel, J., Vierkant, P., Ulrich, R., Kloska, G., Schnepf, E.,Fichtmüller, D. et al. (2015): Metadata Schema for the Description ofResearch Data Repositories: version 3.0 (29), doi: 10.2312/re3.008Silvello, G. (2018). Theory and practice of data citation. *Journal ofthe Association for Information Science and Technology, 69*(1) 6-20.doi: 10.1002/asi.23917Starr, J., Castro, E., Crosas, M., Dumontier, M., Downs**, R.R.,**Duerr, R., et al. (2015). Achieving human and machine accessibility ofcited data in scholarly publications, *PeerJ Computer Science* 1: e1,doi 10.7717/peerj-cs.1Tonkin, E., (2009). MetRe [supporting the metadata revisionprocess.](https://research-information.bristol.ac.uk/en/publications/metre-supporting-the-metadata-revision-process(b2fa9a79-e50b-4888-b510-336aacf73da5).html)*International Conference on Digital Libraries*,Vardigan, M., Heus,P., & Thomas, W. (2008). Data documentationinitiative: Toward a standard for the social sciences. *InternationalJournal of Digital Curation. **3*****(1). doi:**[10.2218/ijdc.v3i1.45](https://doi.org/10.2218/ijdc.v3i1.45)Whyte, A. & Wilson, A. (2010). How to appraise and select research datafor curation. *DCC How-to Guides. Edinburgh*: Digital Curation Centre.http://www.dcc.ac.uk/resources/how-guidesWilkinson, M.D.,[Dumontier](https://www.nature.com/articles/sdata201618#auth-2), M.,Aalbersberg, I.J.J., Appleton, G., Axton, M., Baak. A., et al. (2016).The FAIR guiding principles for scientific data management andstewardship, *Scientific Data, 3*, 160018. doi: 10.1038/sdata.2016.18[^1]: The FAIR Guidelines have been extended from scholarly texts to    data sets (Wilkinson,    [Dumontier](https://www.nature.com/articles/sdata201618#auth-2), et    al., 2018).[^2]: <https://datacite.org/>[^3]: <https://www.w3.org/TR/vocab-dcat/>[^4]: Such operators need to be unambiguous. For example, Digital Object    Identifiers (DOIs, <http://doi.org>) were developed for scholarly    journals and are assigned by publishers, with a part of the DOI code    being a unique publisher ID. While the DOIs may identify more than    one data set, version numbers distinguish the data sets. For    instance, the entire GSS (General Social Survey) has only one DOI,    but it is possible to drill down through the different data sets by    specifying version numbers.[^5]: Schema.org is a project of a consortium of search-engine    companies. The Schema.org dataset schema    (<https://schema.org/Dataset>) is used by the Google Data Search.[^6]:[^7]: https://www.w3.org/TR/vocab-dcat/[^8]: <https://schema.datacite.org/>[^9]: <https://www.fgdc.gov/>[^10]: <https://wiki.dbpedia.org/>[^11]: <https://www.icpsr.umich.edu/icpsrweb/>[^12]: <https://www.ddialliance.org/>. Note that the Data Documentation    Initiative (DDI) is different from the Data Discovery Index (DDI)    associated with DataMed.[^13]: [https://www.cessda.eu/]{.underline}[^14]: <https://www.europeansocialsurvey.org/data/>[^15]: The Australia National Data Service, <https://www.ands.org.au/>[^16]: There are additional collections at <http://data.census.gov>,    <http://gss.norc.org>. [ ]{.underline} <http://electionstudies.org>,    <http://psidonline.isr.umich.edu>, and <http://www.nlsinfo.org>.[^17]: <https://www.earthcube.org/>[^18]: <https://pds.nasa.gov/>[^19]: <https://www.uniprot.org/>[^20]: <http://www.rcsb.org/>[^21]: <https://datadryad.org/>[^22]: <https://www.openarchives.org/pmh/>[^23]: <https://www.colectica.com/>[^24]: <https://gssdataexplorer.norc.org/>[^25]: <http://wiss-ki.eu>[^26]: <http://www.dcc.ac.uk/>[^27]: <http://irods.org>[^28]: <http://schema.org/dataset/datastreams>[^29]: The term micro-data is used in two distinct ways. In the context    of HTML, it is associated with embedding Schema.org codes into web    pages similar to micro-formats. In the context of survey data, it    refers to individual-level data.[^30]: <https://mmisw.org/>[^31]: <https://www.re3data.org/>[^32]: <https://joinup.ec.europa.eu/release/dcat-ap/11>[^33]: E.g., Online Analytical Processing (OLAP), Enterprise Data    Warehouses (EDW), and Decision Support Systems (DSS).[^34]: <https://www.w3.org/TR/vocab-data-cube/>[^35]: <https://www.myexperiment.org/home>[^36]: <https://www.crossref.org/>[^37]: <https://orcid.org/>[^38]: <https://duraspace.org/vivo/>[^39]: <https://www.microsoft.com/en-us/research/project/microsoft-academic-graph/>
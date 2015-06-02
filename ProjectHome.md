TAMELizer is a general test engine for XML content testing. It can verify structural and semantic constraints (including arithmetic and date calculations), compatibility across documents, and other content profiles. However the focus is more on rules and constraints - within and across documents - than on expressing or enforcing document structure (e.g. using schema-like representations). TAMELizer leverages the expression power of XPath2.0 and of its libraries. The basic unit of test expression and of test execution is the <b>test assertion</b> that can be seen as a rule (either semantic and syntactic) over and across XML artifacts and documents.

TAMELizer uses an approach different from existing XML test tools more specialized on document testing, because the XML artifacts it processes can represent any kind of entity subject to testing in addition to business documents: catalogs, metadata files, schemas, configuration files, monitor captures, output of previous tests, and test definitions themselves. Handling combinations of such artifacts requires strong correlation and consistency checking between XML artifacts (document or smaller), and fine-grain reporting capabilities. Such artifacts are often used in the testing of software systems and applications - e.g. for conformance to a standard or a specification. Often, such testing can be decomposed into:
<ul><li>(Phase 1) an operational phase where test scenarios are run against the system under test.</li>
<li>(Phase 2) an analysis phase where a conformance (or interoperability) assessment is made based on the operational outcome of Phase 1. </li></ul>
TAMELizer is intended to support phase (2) by analyzing the XML-formatted output of (1), which usually requires processing and correlating a combination of above-mentioned artifacts.

The underlying model uses conventional test constructs: a test suite is defined as a workflow of individual test cases, here executable test assertions. The innovation is in leveraging XPath and XSLT for expressing and processing these test assertions. Every test assertion is a separate test unit to be reported on, but also as a rule that can be subject to inferences: an embedded forward-chaining rule engine automatically combines and orders test assertions into logical workflows (e.g. "do test B only if test A was successful on a particular test target"). A test assertion can also "summarize" the results of a group of test assertions.

The TAMELizer project is funded and maintained by <b>Fujitsu America, Inc</b>. in order to promote the development of test assertions and to facilitate and standardize the testing of software systems and applications (not just business documents).  The project is small enough that the entire code (XSLT scripts) its documentation and some examples are packaged with every download - no management via version control at this time. The entire project is scripted in XSLT2.0, except for the HTML report rendering sheet which is XSLT1.0.

The test assertions - or rules - are based on the Test Assertions Guideline XML mark-up TAML (http://docs.oasis-open.org/tag/taml/v1.0/cs02/testassertionmarkuplanguage-1.0-cs02.pdf), from the OASIS Test Assertions Guideline (TAG) TC (http://www.oasis-open.org/committees/tc_home.php?wg_abbrev=tag).

The TAG methodology for writing test assertions is described in:
(http://docs.oasis-open.org/tag/guidelines/v1.0/cn01/guidelines-v1.0-cn01.pdf).

The overall Test Assertion Model is an OASIS standard:
(http://docs.oasis-open.org/tag/model/v1.0/os/testassertionsmodel-1.0-os.pdf)

More precisely the test assertions are an XPath2.0 extension - "TAML-X" - of the TAML mark-up language. TAML-X (or TAML for XPath) was defined by the authors based on the work from TAG in OASIS.
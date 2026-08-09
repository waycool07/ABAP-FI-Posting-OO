# ABAP-FI-Posting-OO
Report ZFI_POSTING_SW handles user input, and creates LCL_REPORT which maintains a reference to the generic base class ycl_fi_interfaces.<br />
The runtime object with help of factory decides which concrete implementation to instantiate.<br />
The current implementation focuses on Excel. The same design can be extended with additional implementations such as CSV or XML while continuing to expose them through the common YCL_FI_INTERFACES reference.<br />
<br />Below Concepts are demonstrated in the prototype:<br />
Inheritance & Method Redefinition<br />
YCL_FI_INTERFACES_EXCEL inherits from YCL_FI_INTERFACES and redefines Excel-specific behavior.<br />
<br />Upcasting<br />
The Excel implementation is handled through a reference to YCL_FI_INTERFACES.<br />
<br />Common Functionality<br />
The base class contains reusable processing such as common file handling, data preparation, date conversion and ALV-related functionality, while the child class provides implementation-specific behaviour.<br />
<br />Upcasting<br />
<br />Downcasting<br />
<br />FI Posting<br />
The application prepares the FI document structures and posts the document using BAPI_ACC_DOCUMENT_POST <br />
Note:<br />
This is a learning/prototype project focused on applying OO ABAP concepts to an FI posting scenario. It is not intended as a production-ready framework.<br />

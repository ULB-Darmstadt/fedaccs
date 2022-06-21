# fedaccs
general information for the folio federated access (fedaccs) project 

<!-- TOC start -->
  * [Project ](#project)
  * [Stripes UI Modules](#stripes-ui-modules)
    + [stripes-core](#stripes-core)
    + [ui-sso](#ui-sso)
    + [ui-tenant-settings](#ui-tenant-settings)
  * [Backend module](#backend-module)
    + [mod-login-saml](#mod-login-saml)
  * [Remarks on further use](#remarks-on-further-use)
<!-- TOC end -->
<!-- TOC --><a name="fedaccs"></a>

<!-- TOC --><a name="project"></a>
## Project 
The project was funded by the **"Innovation Fund of the Hessian Ministry of Science and the Arts"** and managed by the **University and State Library (ULB)** of the Technical University Darmstadt (TU). We have cooperated with the company **Knowledge Integration, Sheffield**.

It was dedicated to the legal and technical aspects of a cooperative usage scenario involving
several libraries. The background to this is the increasing number of cooperative degree programs and the use of large
libraries by users which are not members of the library's home institution, primarily students in metropolitan areas. At the end was
a prototypical implementation in the open source library system FOLIO.

<!-- TOC --><a name="stripes-ui-modules"></a>
## Stripes UI Modules
<!-- TOC --><a name="stripes-core"></a>
### stripes-core
*based on clone of FOLIO repo*\
Changes made to this project required to support “public” pages. I.e. Pages visible without login in stripes. This was necessary for the alternate PoC sign in page added by the “ui-sso” project below.\
https://github.com/ULB-Darmstadt/stripes-core/tree/fedaccs

<!-- TOC --><a name="ui-sso"></a>
### ui-sso
*new repo*\
Adds alternate public page for sign in that can talk to the federation-aware version of mod-login-saml and handle multiple accepted IDPs. If the PoC was to become a fully accepted project and work done to make it part of the folio eco-system, then the work on the login page in this module could be folded into the default login page.\
https://github.com/ULB-Darmstadt/ui-sso

<!-- TOC --><a name="ui-tenant-settings"></a>
### ui-tenant-settings
*based on clone of FOLIO repo*\
Contains extensions for the extra configuration available when using SSO.\
https://github.com/ULB-Darmstadt/ui-tenant-settings/tree/fedaccs

<!-- TOC --><a name="backend-module"></a>
## Backend module
<!-- TOC --><a name="mod-login-saml"></a>
### mod-login-saml
*based on clone of FOLIO repo*\
Customizations in this module provide the ability to understand Federated metadata as well as other improvements over how the module was structured.\
https://github.com/ULB-Darmstadt/mod-login-saml/tree/fedaccs

<!-- TOC --><a name="remarks-on-further-use"></a>
## Remarks on further use
Note that you have to use the branch **fedaccs** in the 3 cloned FOLIO repositories.\
We didn't merge our changes to the master branches of the cloned FOLIO repos.\
If you wish to use our work in your FOLIO environment you'll have to merge and face potential merge conflicts and test errors as we didn't touch existing tests.


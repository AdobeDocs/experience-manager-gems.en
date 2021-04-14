---
title: Content Package Validation Improvements
description: Based on the customer issues in deploying maintenance updates some improvements have been made in Granite Package Maven Plugin & AEM Package Manager.
uuid: ef69d957-6898-42cf-8c2f-fd676a13a340
discoiquuid: 12574219-5f31-4cb3-bdff-e8d64636841e
internal: true
targetaudience: target-audience advanced
---

# Content Package Validation Improvements{#content-package-validation-improvements}

>[!VIDEO](https://video.tv.adobe.com/v/19656/?quality=9)

*Delivered May 24, 2017*

* Improvements made in Granite Package Maven Plugin ensure that maintenance updates are properly packaged
* Package Manager now provides an option to pre-validate a package before actually installing it.
* Some details:

    * Improvements in Package Manager:

        * CQ-81729 :Often a fix in CFP/SP doesn’t work as CFP/SP contains content file (JSP or JS file) which is customized and overlaid in /apps by customer.  
          Using an option under validate button in package manager, customer can  
          validate that no overlay is effected and identify overlays that need to  
          be updated.
        
        * CQ-91005 : Sometimes after installing a package some bundles remain in installed state due to unresolved imports. Using an option under validate button in package manager, customer can validate that installing the package  
          will not result in bundles in installed state and also identify the  
          affected bundle & unresolved imports.

    * Improvements in granitepackage-maven-plugin:

        * CQ-102349 : Index definition in a CFP/SP package can cause re-indexing which can take long time on large repositories. To ensure that index definitions  
          are not included in a package, a flag is provided that will cause a  
          build failure if it detects that package contains index definition.   
        
        * CQ-74198 : Check whether the dependencies (hotfix/featurepack/servicepack only) mentioned are actually existing & whether the group versions match  
          (i.e. a 6.1 HF should not have dependency on 6.0 HF). Fails the build if  
          found violating.

Presented by:

* Gurpreet Singh Bhatia, Lead Software Engineer, AEM Sustaining Engineering, Adobe
* Karanjeet Singh, Senior Software Engineer, AEM Sustaining Engineering, Adobe

Presenter Slides

[Get File](assets/granite-gems-content-package-validation-improvements05242017.pdf)

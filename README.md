# TMWebServices
*Prequisites for using our framework:
        1.Download web.xml and place it in folder (\WEB-INF)
        ---------------------------------------------------------------------------------------------------------------------
        2.In \WEB-INF\classes folder create a file named ServiceConfiguration.conf 
                                                             -Data in file must be in JSON format mentioned as below
                                                              { packages:["package 1","package 2",..,"package n"] }
                                                              where package1,package2,package3 are package names where your services                                                                    resides.
        -----------------------------------------------------------------------------------------------------------------------
        3.Dependencies to add in \WEB-INF\lib folder are as follows:
                                                             -TMWebService.jar.
                                                             -itext jar file. 
                                                             -gson jar file.    
                                                     Note:-Files are available above for downloading. 
 
 --------------------------------------------------------------------------------------------------------------------------------------
 
 
 *framework entities
        1.Interface:- WebServiceInterface (in package, com.thinking.machines.interfaces)
        2.Service Class:- TMService (in package, com.thinking.machines.servlets)
        3.Annotations:- a:- @Path(value) along with service Class and Method
                        b:- @RequestData(value) on method perameters to get respective data similar to value from request
                        c:- @Forward(value) to forward request to respective value it might be to another service or jsp,html.
                        d:- @ResponseType("value") along with service Method in these case value is "text/html" or "json" or                                     "application/pdf" or "none"
                        e:- @Secured("className along with package name") here only name of those class which implements                                          WebServiceInterface and define 2 method which is declared in WebServiceInterface                       
                        f:- @Upload
                             (all anotations lies in package com.thinking.machines.annotations.* )
                       d:-Upload(value)
 
 ----------------------------------------------------------------------------------------------------------------------------------------
 
 
 *Helpfull funtionalities:-
       1.You can get report of your work done of usage of our framework by using url (..../service/report)
              -As an result report will get save in WEB-INF\report folder as Service.pdf
       2.While using our framework if any kind of mistake done than you can get upto it by browsing an pdf file get generated in \WEB-             INF\report folder named error.pdf which include errors with their occurence reasons.
 
 
 
 -------------------------------------------------------------------------------------------------------------------------------------
 
 *Constraints:-
        1.Request must be of type POST only.
        2.Services should have one perameter only, if you need we can inject dependencies(ServletContext, HttpServletRequest,HttpServletResponse).
        
========================================================================================================================================

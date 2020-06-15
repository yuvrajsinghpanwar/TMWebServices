# TMWebServices
*Prequisites for using our framework:</br>
========================================================

 1 .Download web.xml and place it in folder (\WEB-INF)</br></br>
 2.In \WEB-INF\classes folder create a file named ServiceConfiguration.conf</br> 
 -Data in file must be in JSON format mentioned as below</br>
 {</br> 
 packages:["package 1","package 2",..,"package n"] </br>
 }</br>
 where package1,package2,package3 are package names where your services resides.</br></br>
 3.Dependencies to add in \WEB-INF\lib folder are as follows:</br>
 -TMWebService.jar.</br>
 -itext jar file. </br>
 -gson jar file.    </br> 
 Note:-Files are available above for downloading.(in WEB-INF/lib/*) </br></br>
 
 YOU CAN REFER TO ABOVE MENTIONED WEB-INF directory to understand these prequisites.
 =====================================================================================
---------------------------------------------------------------------------------------------------------------------------------------- 
 
*framework entities
====================
        1.Interface:- WebServiceInterface (in package, com.thinking.machines.interfaces)</br>
        2.Service Class:- TMService (in package, com.thinking.machines.servlets)</br>
        3.Annotations:- a:- @Path(value) along with service Class and Method</br>
                        b:- @RequestData(value) on method perameters to get respective data similar to value from request</br>
                        c:- @Forward(value) to forward request to respective value it might be to another service or jsp,html.</br>
                        d:- @ResponseType("value") along with service Method in these case value is "text/html" or "json" or       </br>                              "application/pdf" or "none"</br>
                        e:- @Secured("className along with package name") here only name of those class which implements     </br>                                     WebServiceInterface and define 2 method which is declared in WebServiceInterface                    </br>   
                        f:- @Upload</br>
                             (all anotations lies in package com.thinking.machines.annotations.* )</br>
                       d:-Upload(value)</br>
 
 ----------------------------------------------------------------------------------------------------------------------------------------
 
 
 *Helpfull funtionalities:-</br>
 ===============================
      1.You can get report of your work done of usage of our framework by using url (..../service/report)</br>
              -As an result report will get save in WEB-INF\report folder as Service.pdf</br>
       2.While using our framework if any kind of mistake done than you can get upto it by browsing an pdf file get generated in \WEB-             INF\report folder named error.pdf which include errors with their occurence reasons.</br>
 
 
 
 -------------------------------------------------------------------------------------------------------------------------------------
 
 *Constraints:-</br>
 =========================
        1.Request must be of type POST only.</br>
        2.Services should have one perameter only, if you need we can inject dependencies(ServletContext, HttpServletRequest,HttpServletResponse).</br>
        
========================================================================================================================================

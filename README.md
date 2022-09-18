# JAX-WS Client Generator Maven Project

An opinionated maven project to create static JAX-WS clients from `.wsdl` definition files. [cxf-codegen-plugin](https://cxf.apache.org/docs/maven-cxf-codegen-plugin-wsdl-to-java.html) is used for generating client libraries.

## Usage

1. Clone this project.
2. Create a new maven module with a similar structure to the `example_globalweather` project.
3. Copy the `.wsdl` file to the module's directory.
4. Modify root `pom.xml` and change `<groupId>` with the desired package name.
5. Modify module's `pom.xml` and change parent `<groupId>` with the desired package name(must be the same with root `<groupId>`) and change child `<artifactId>` with module's name.
6. Add your new module to root `pom.xml`
7. (Optional) Change Java version or **extraarg** parameters in the `pom.xml`
8. Run `mvn package` command to generate web service client jars.
9. Go to `<module_name>/target` folder to access .jar files.

## Enabled plugins

* **value-constructor**: https://github.com/javaee/jaxb2-commons/tree/master/value-constructor
* **fluent-api**: https://github.com/javaee/jaxb2-commons/tree/master/fluent-api
* **JAXB2 Setters**: https://github.com/highsource/jaxb2-basics/wiki/JAXB2-Setters-Plugin
* **JAXB2 SimpleHashCode**: https://github.com/highsource/jaxb2-basics/wiki/JAXB2-SimpleHashCode-Plugin
* **JAXB2 SimpleEquals**: https://github.com/highsource/jaxb2-basics/wiki/JAXB2-SimpleEquals-Plugin
* **JAXB2 FixJAXB1058**: https://github.com/highsource/jaxb2-basics/wiki/JAXB2-FixJAXB1058-Plugin

## About the example

Example `.wsdl` has taken from [Example WSDL file: globalweather.wsdl](https://www.ibm.com/docs/en/api-connect/10.0.x?topic=api-example-wsdl-file-globalweatherwsdl) for solely demonstration purpose.


Algunes dependàncies d'aquest Plugin interfereixen amb WS, per això s'han d'excloure.


        <dependency>
            <groupId>org.fundaciobit.plugins</groupId>
            <artifactId>plugin-documentcustody-alfresco</artifactId>
            <version>5.0.0-SNAPSHOT</version>
            <exclusions>
              <exclusion>
                <groupId>org.slf4j</groupId>
                <artifactId>slf4j-api</artifactId>
              </exclusion>
              <exclusion>
                <groupId>javax.xml.stream</groupId>
                <artifactId>stax-api</artifactId>
              </exclusion>
              <exclusion>
                <groupId>xpp3</groupId>
                <artifactId>xpp3</artifactId>
              </exclusion>
					 </exclusions> 
        </dependency>
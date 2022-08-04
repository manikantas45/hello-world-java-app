This is my fixed for DPLM-
For any questions - Please email me at DevOps@Bibhutibhusan.xyz
# ========================NEXUS==============================

<distributionManagement>
	<repository>
		<id>deploymentrepo</id>
		<name>Internal Releases</name>
		<url>http://192.168.0.50:8081/nexus/content/repositories/MPH/</url>
	</repository>
 
	<snapshotRepository>
		<id>deploymentrepo</id>
		<name>Internal Releases</name>
		<url>http://192.168.0.50:8081/nexus/content/repositories/MPH-SNAP/</url>
	</snapshotRepository>

</distributionManagement>


=====================SETTING.XML=================================
   <server>
		<id>deploymentrepo</id>
		<username>deployment</username>
		<password>deployment123</password>
</server>

=======================Setting.xml with Artifactory Setup======================
<mirror>
      <id>central</id>
      <name>Maven Repository Manager running on repo.mycompany.com</name>
      <url>http://13.127.94.210:8081/artifactory/list/group/</url>
      <mirrorOf>*</mirrorOf>
    </mirror>
#end

# Maven Introduction

- Maven is a Build tool
- It always produces an artifact and helps in managing dependencies
- It can also be handled as a Project Management Tool
- It handles versioning and releases
- Describes what your project is doing and what it produces
- Can easily produce Javadocs as well as other site information
- We can recreate builds for any environment
- While downloading the dependencies it will also pull other items it needs
- Maven contains almost everything needed for your environment
- Works with local repo
- Works with IDE and standalone as well
- Preferred choice for working with build tools like Jenkins, Bamboo, etc..
- Sometimes we also hear about or work with ANT. There are some different behaviors and functions of both these tools

- ***ANT***
	- ANT was developed to be a replacement for a build tool called Make
	- Designed to be cross platform
	- Built on top of Java and XML
	- Very procedural
	- ANT really isn't a build tool as much as it is a scripting tool as we have to do everything explicitly.

	```
	<target name="clean" description="clean up">
		<!-- Delete the ${build} and ${dist} directory trees -->
		<delete dir="${build}" />
	</target>
	```
	
	- We have to define everything that we want to do
	- A lot of tribal knowledge, nothing caries over
- ***Maven***
	- Maven is a full fledged build tool
	- A lot of implicit gunctionality
	- Consistancy across projects
	- Also capable to archive inheritance in project
	- Transitive dependencies
	- Build around versioning
	- Better IDE integration
	- Convention over configuration
	- Less overheard through use of repos

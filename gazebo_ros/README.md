
# Upgrade gazebo5 from gazebo (default installed):

1. Remove default gazebo:
	sudo apt-get remove gazebo_version
	ex. sudo apt-get remove gazebo2.1

2. After successfully removing default/old gazebo, install new version gazebo:
	sudo apt-get install gazebo_new_version
	ex. sudo apt-get install gazebo5.0

3. Inculde path of configuration files in CMakeLists.txt:
	set(GAZEBOINCLUDEDIRS /usr/include;/usr/include/gazebo-5.0;/usr/include/sdformat-2.3) 
	set(GAZEBOLIBRARYDIRS /usr/lib/x86_64-linux-gnu;/usr/lib/x86_64-linux-gnu/gazebo-5.0/plugins)
	
	Note that: Mannually check this path, make it out correct path.

4. Modify package.xml:
	Edit build and run depend of gazebo version 
	ex: <build_depend>gazebo5</build_depend> 
	    <run_depend>gazebo5</run_depend> 
	
	Add build and run depend of gazebo version
	ex: <build_depend>libgazebo5-dev</build_depend> 
	    <run_depend>libgazebo5-dev</run_depend>


# VDrive-Graph-Visualization
Graph visualization prototype implementation with focus on visualization-driven data reduction and graph streaming.

## Requirements
- Hadoop 2.7.7
- Apache Flink 1.10.0
- Java 1.8

## Install
Install Hadoop 2.7.7 and Apache Flink 1.10.0 on the machine that runs the flink cluster. 
Clone the repository to a local file system on the machine that runs the visualization.

## Usage
Make sure HDFS and the flink cluster are running and graph data is stored in HDFS.
The jar file contained in this repository is non-executable and contains class information for the flink cluster.
This jar file needs to be merged with the following jars that can be download from the maven central repository:
- gradoop-flink-0.5.2.jar
- gradoop-common-0.5.2.jar
- flink-gelly_2.11-1.7.2.jar

Load the maven project into a Java IDE and run the Main.java file with the path of the merged jar file as -j argument.
Open the graphical user interface in browser.
Insert parameters as requested by the GUI.

- Cluster Address: DNS host name of the flink cluster running machine.
- HDFS Address: DNS host name of the HDFS master node.
- HDFS Port: HDFS entry point of the HDFS master node.
- Data Dir: Path to graph files in HDFS directory.
- Graph ID: Gradoop Graph ID (only necessary for 'Gradoop' backend)

Start the visualization by selecting a backend architecture.
Visual operations (zoom, pan) can be triggered with a hand-held pointing device (e.g. computer mouse).

#### Backend architectures
Graph data has to be stored in Hadoop distributed File System (HDFS).
If you want to visualize graphs in Gradoop CSV format (https://github.com/dbs-leipzig/gradoop/wiki),
choose 'Gradoop' to start the visualization.
If you want to visualiza graphs in VDrive format,
choose 'TableStream' or 'AdjacencyMatrix'.

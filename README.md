Download Link: https://assignmentchef.com/product/solved-cse102-homework-10-coordinate-system
<br>
In this assignment, you are going to use structures to describe and perform computations on simple 2D geometric objects placed on Euclidean space (coordinate system). You will be using <strong>points, lines, and polygons.</strong> You will read the definitions of a given set of geometric structures and actions to be performed on them from an input file. The results of the actions will be printed into an ouput file.

<strong>Input File:</strong>

The input file has two parts: data and actions.

<ul>

 <li>Data:

  <ul>

   <li>Data part starts with keyword “data” (a single line).</li>

   <li>It is followed by a number indicating the number of 2D objects to be read.</li>

   <li>Following each line will have a 2D object definition. See below for definition of 2D objects.</li>

   <li>You can assume that there will be at least 1 and at most 100 2D objects.</li>

   <li>You can assume that the object names are unique (no replications).</li>

  </ul></li>

 <li>Actions:

  <ul>

   <li>Action part starts with keyword “actions” (a single line).</li>

   <li>It is followed by a file name indicating where the results of the actions will be output.</li>

   <li>This is followed by a number indicating the number of actions.</li>

   <li>Following each line will have an action. See below for definition of 2D actions and what they should generate.</li>

  </ul></li>

 <li>Comments:

  <ul>

   <li>Any part of the input file can include a comment which should be discarded during reading. The comments starts with “\” and ends at the end of the line.</li>

  </ul></li>

</ul>

Example input and output files are provided as attachements.

<strong>2D Objects</strong>: There are three kinds of geometric objects.

<ul>

 <li>Point: A point is defined by its two coordinates and a name. I.e.,

  <ul>

   <li>0 100.0 P1 // A point at location (100,100) with name “P1”.</li>

   <li>0 200.0 P2 // A point at location (100,100) with name “P2”.</li>

  </ul></li>

 <li>Line: A line is defined by two points and a name. I.e.,

  <ul>

   <li>P1 P2 L12 // The line named “L12” defined by two end points “P1” and “P2P).</li>

  </ul></li>

 <li>Polygons: A circularly connected set of lines with at most 20 components. It can be defined either by connecting a set of points or a set of lines. I.e.,

  <ul>

   <li>P1 P2 P3 P4 PG4 // The polygon “PG4” defined by four lines connecting first “P1” and “P2”, second “P2” and “P3”, third “P3” and “P4” and finaly “P4” and “P1”.</li>

   <li>L12 L23 L31 P4 PG3 // The polygon “PG3” defined by three lines “L12”, “P23” and “L31” in the given order.</li>

  </ul></li>

</ul>

<strong>Actions</strong>: The following actions can be defined over the 2D objects provided in the data part of the file.

<ul>

 <li>Distance: Print the distance between two points. For example, the following action should result in the given output.

  <ul>

   <li>Distance P1 P2 // Print out the distance between points “P1” and “P2”.</li>

  </ul></li>

</ul>

Distance(P1,P2) = 12.0

<ul>

 <li>Distance: Print the distance between a point and a line. For example, the following action should result in the given output.

  <ul>

   <li>Distance P1 L12 // Print out the distance between point “P1” and line “L12”.</li>

  </ul></li>

</ul>

Distance(P1,L12) = 1.1

<ul>

 <li>Angle: Print the angle (in degrees) between two lines. For example, the following action should result in the given output.

  <ul>

   <li>Angle L1 L2 // Print out the angle between lines “L1” and “L2”.</li>

  </ul></li>

</ul>

Angle(L1,L2) = 81.0

<ul>

 <li>Length: Print the length of a given line. For example, the following actions should result in the given output.

  <ul>

   <li>Length L1 // Print out the length of line “L1”.</li>

  </ul></li>

</ul>

Length(L1) = 5.8

<ul>

 <li>Length: Print the length (circumference) of a given polygon. For example, the following actions should result in the given output.

  <ul>

   <li>Length PG1 // Print out the circumference of the polygon “PG1”.</li>

  </ul></li>

</ul>

Length(PG1) = 15.2

<ul>

 <li>Area: Print the area of a given polygon. For example, the following actions should result in the given output.

  <ul>

   <li>Area PG1 // Print out the area of the polygon “PG1”</li>

  </ul></li>

</ul>

Area(PG1) = 144.4

We strongly encourage you to use structures and nested structures and arrays. While grading we will also look for the use of <strong>pass by reference</strong> (using as default parameter passing strategy. Your grade will also be affected by your choice of design. Finally,  if you can not implement a given functionality, print NOT_IMPLEMENTED in the output file.
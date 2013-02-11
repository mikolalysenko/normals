normals
=======
Estimates normals for surface meshes.

Installation
============
Using [npm](https://npmjs.org/):

    npm install normals
    
Example
=======
Here is how to compute the vertex and face normals for the Stanford bunny:

    var bunny = require("bunny");
    var bunny.vertexNormals = require("normals").vertexNormals(bunny.positions, bunny.faces);
    var bunny.faceNormals = require("normals").faceNormals(bunny.positions, bunny.faces);

`require("normals").vertexNormals(cells, positions)`
----------------------------------------------------
This estimates the vertex normals for an oriented mesh.

* `positions` is an array of vertex positions
* `faces` is an array of indexed vertex positions

Returns: An array of length = `positions.length` of the per-vertex normals.


`require("normals").faceNormals(cells, positions)`
----------------------------------------------------
This estimates the face normals for an oriented mesh.

* `positions` is an array of vertex positions
* `faces` is an array of indexed vertex positions

Returns: An array of length = `faces.length` of the per-face normals.


Credits
=======
(c) 2013 Mikola Lysenko. BSD
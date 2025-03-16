## What is Three.js:
ThreeJS is opensource javascript library that simplifies the process of rendering 3D graphics in the browser.
It provides abstraction over WebGL, make 3D rendering easier

## How Three.js Simplifies WebGL Development:

WebGL is powerfull, but working with WebGL always need a lot of boilerplate code, that cost a lot of effort.
ThreeJS abstracts almost of complexity by some of concept like Scene, Meshes, Materials, Geometry, Camera... etc
ThreeJS have some 3D objects pre-built: Cubes, Spheres, Planes, saving developer time.
ThreeJS have some pre-built loader that able to load 3D models ( OBJ, FBX that exported from some 3D models software like Blender, Autocard etc... )
ThreeJS have build-in features for Lighting, shadows, Textures: 
    Lighting: ambient, directional, point, spotlights, etc.
    Shadows and materials: mesh basic, phong, lambert, standard, and physical materials
ThreeJS support animations and effects.

# Scene
    A container contain all object in 3D world, the object was arrange as a tree.
# Camera 
    Define a viewpoint or perspective from which the scene is viewed.
    ThreeJS support perspective camera and orthographic camera 
# Renderer
    WebGLRenderer is the most commonly used renderer in Three.js which abstract for WebGL.
# Mesh 
    A virtual concept represent the things that will be draw on scene. It 's combine Geomertry and Material :
    `const geometry = new THREE.BoxGeometry();
    const material = new THREE.MeshBasicMaterial({ color: 0x00ff00 });
    const cube = new THREE.Mesh(geometry, material);`
# Geometry
    Define the shape of mesh ( cubes, spheres, planes)
    We can define our custom Gemetry by defined the vertices, faces, normal which help rendering engine understand how to display the shape correctly.
# Material
    Define the appearance of a mesh by determining how it interacts with the light:
    Some of existing Material: 
        MeshBasicMaterial
        MeshLambertMaterial
        MeshPhongMaterial
        MeshStandardMaterial
    Mesh have properties like: color, opacity, and textures.
## What are the advantages of using Three.js over raw WebGL?
    1. Abstraction of Low-Level WebGL Code
    2. Cross-Browser Compatibility
    3. Simplified Scene Management
    4. Built-in Geometries and Materials
    5. Advanced Rendering Features
    6. Animation and Movement
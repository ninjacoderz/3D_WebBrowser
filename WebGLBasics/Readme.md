## What is WebGL?

WebGL (Web Graphics Library) is a JavaScript API that allows developers to render 3D graphics directly in a web browser without the need for plugins. It provides a low-level, hardware-accelerated 3D rendering context using the GPU, based on OpenGL ES (a simplified version of OpenGL used for mobile and embedded devices). WebGL is widely supported by modern browsers and enables interactive 3D and 2D graphics in websites.

WebGL works within the browser's HTML5 <canvas> element, allowing for the rendering of 3D scenes and objects, along with complex visual effects such as lighting, shadows, and textures. By directly accessing the graphics hardware (GPU), WebGL ensures smooth performance and the ability to handle complex 3D graphics.

## Differ with Traditional 2D Web Graphics 
# Canvas API:
    Usage: Canvas tag provide some API for manupulate with it's content. It provide some draw functions ex: drawImage, lineTo, fill etc... They are very basic 2D drawing.
    Rendering Model: Pixel based, directly manupulate pixels in buffer, and swap buffer to show things.
    Performance: Very sufficient for 2D, but limitted or very complex in 3D.
    Complexity: Simple with 2D graphics, not require to have any knowlegde about GPU and computer graphic.
# SVG:
    Usage: Fix disadvance of Pixel-base, it render base on Vector based ( lines, curves, text, etc...)
    Rendering Model: base on browser native engine, browser auto convert vector base to draw them to scene.
    Performance: Effective with 2D, not effect with large amount of elements.
    Complexity: Easy to learn, manupulate via Javascript and css, use for interactive charts icons, and simple animation.
# WebGL: 
    Usage: Design for 3D graphic, interactive directly with GPU
    Rendering Model: use graphic pipeline to processes vertices, apply transformation, then render final images.
    Performance: Very effective with complex 3D scenes, textures, lighting, shaders, suitable for gaming , simulations, other high-performance visual applications.
    Complexity: Require more knowledge about computer graphics, need deep understand about shaders, buffers, matrices. More complex than others.

## Graphic pipeline:
    Refer for the steps that computer rendering an image from raw data to a final rendered image that can display on screen. There are a main stages of pipeline:
# Vertex Processing: 
    Responsible tof transforming vertext possitions ( translation, rotate, scaling etc.. ), calculate lighting, normals, texture coordinate.
# Primitive Assembly:
    GPU assembles the vertices in to primitives ( point, lines, triangle), one of the most frequently primitives use is Triangle.
# Rasterization: 
    Convert geometric data to pixels that actually show on screen, it 's determine with pixel will be shown on screen.
# Fragment process:
    Fragment shder determine its final color, transparency, texture, and lighting effects. The fragment shader computer the appearance of each pixel base on information like texture, light, meterial properties.

## Role of shaders in WebGL
    Shader is small programs written in specialized languages that run on GPU. Allow parrallel proccessing of vertices and fragments. 
# Vertex Shader
    First stage in graphic pipeline, 
    Process each vertex of a 3D object, transform vertices in to 2D screen ( by using view mode, projection matrics )
    Handle other vertex compute: lighting, nomals, texture, etc... )
    Outpute from vertex shader include transformed vertext possitions, along with data passed to the fragment shader.

# Fragment Shader
    Responsible for processing fragment( potential pixels ) that will able to draw on screen. 
    Determines the final color of the pixel
    It can use some lighting , textures , shadows, reflections to create realistic visuals
    Receive input is vertex and output the color for each fragment
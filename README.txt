In this tutorial we introduce the BufferCPU class.
It will help us make chunks of memory that Vulkan
can use. We will use this calss to make a Vertex Buffer
and an Index Buffer, which will allow us to render
geometry of any size, and allow us to put the positions
of the vertices on the CPU, rather than in the shader.
We also introduce a file called SquareDataArrays.h, which
holds information about our vertices, like the positions
of each vertex, and the colors of each vertex (colors are
explained in a later tutorial). Inside our Helper class,
we have a new function called memory_from_properties
which will help us make buffers depending on the type
of memory that the computer supports with Vulkan.

We will also be editing the pipelineCreateInfo to have
InputAssembly, which will describe what each vertex is,
and what is inside each vertex (which is just position).

We will also need to change the shader, which is now
called Square.vert, to take in data from the Vertex Buffer
and then use that data to draw geometry
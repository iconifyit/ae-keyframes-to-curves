# cep-ae-keyframes-to-curves

A WIP to convert Adobe After Effects keyframe easings to bezier curves. The work in this extension is based on the [CEP-Boilerplate](https://github.com/iconifyit/cep-boilerplate) framework by Atomic Lotus. The work was influenced by and in some cases guided by:

- [Tomas Šinkūnas](https://github.com/rendertom) a.k.a. Rendertom, who provided insight and guidance on some of the trickier AfterEffects scripting
- [Davide Barranca](https://www.davidebarranca.com) - with a lot of great resources for building CEP panels
- [Hernan Torrisi](http://aescripts.com/bodymovin/) - For insight, guidance, and great code examples.
- [Manny Gonzalez](https://forums.creativecow.net/docs/forums/post.php?forumid=227&postid=27968&univpostid=27968&pview=t) - For great code examples that helped me to understand the concepts.
- [Inspector SpaceTime](https://github.com/iconifyit/inspectorspacetime) - For great code and Doctor Who references and parodies.

## Installation

To install this extension in development mode, open a command line terminal and run `source ./install-dev.sh` (on Mac only). You can also manually copy the entire directory structure (or an alias/symlink) to your Adobe extensions folder.

## Usage

All of the interesting code is in :

- [/cep-ae-keyframes-to-curves/custom/Helpers](/cep-ae-keyframes-to-curves/custom/Helpers)
- [/cep-ae-keyframes-to-curves/custom/info](/cep-ae-keyframes-to-curves/custom/info)

Everything else is just the CEP-Boilerplate framework.

## Current State

The code is only partially functional. Converting keyframe easings to bezier curves is fairly involved as you will be able to tell from the code. Converting one-dimensional keyframes to curves is tricky but not the difficult part. The difficulty is converting keyframes that move at different speeds on the X, Y, and Z axes. To quote @rendertom : 

> "There are Spatial properties ... which makes logic even more complicated. ... Objects in AE can have different speeds/influences for each axis: X, Y, and Z. Meaning, that the object can move one speed on X-axis, but totally different on Y, and some other speed on Z. Therefore you won't get a proper CB result - you should probably get CB curve for each axis, and then average the values". 

I have not done the conversions to calculate the curves on multi-dimensional keyframes. If you would like to contribute, I will be happy to accept pull requests. It would be great to be able to release a complete solution but I already spent way too much time on this (long story) and am not inclined, at present, to spend more time on it but I really hope someone can make use of the work, which has been substantial.
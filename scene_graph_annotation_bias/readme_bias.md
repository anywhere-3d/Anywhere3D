There exist certain biases between the coordinate system used in the annotation interface and the one used in the scene graph. These mainly stem from whether the **x** and **y** coordinates are mean-centered or not, and whether the **z** coordinate is shifted by subtracting the minimum value.  

For **ScanNet**, such biases do not exist. However, they are present in **MultiScan**, **3RScan**, and **ARKitScenes**. We have listed the corresponding offsets in the following files:  
- `multiscan_bias.json`  
- `3RScan_bias.json`  
- `arkitscene_valid_bias.json`  

If you are interested in the data annotation in our interface, you can refer to these offsets to align the annotation interface with the scene graph.  

⚠️ **Note:** For the evaluation of **LLMs**, **VLMs**, and **3D visual grounding models**, you do *not* need to consider these offsets, since the ground-truth 3D bounding boxes we provide are already aligned with each scene’s scene graph.  
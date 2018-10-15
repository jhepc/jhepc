Brain Tumor
===========

Matthew McCormick

.. raw:: html

  <iframe width="560" height="315"
   src="https://www.youtube.com/embed/I2xV0YP1zPI" frameborder="0"
   allow="autoplay; encrypted-media" allowfullscreen></iframe>

Understanding the location and extent of a brain tumor is critical for the prediction of expected symptoms and for the formation of a treatment strategy. This visualization unveils a large tumor in the right, frontal lobe. Blood vessels, which are landmarks and critical structures to avoid during surgery, have been enhanced in from the original magnetic resonance image (MRI). The tumor is highlighted through segmentation in this gradient-based volume rendering.

Vessels in this MRI are enhanced by computing the image Hessian, then examining the magnitude and relative size of the Hessian's eigenvalues. These conditions define a metric for tube-like structures. For more information, see:
Alejandro F. Frangi, Wiro J. Niessen, Koen L. Vinc and Max A. Viergever (1998), "Multiscale Vessel Enhancement Filtering", Medical Image Computing and Computer-Assisted Interventation — MICCAI’98 Lecture Notes in Computer Science 1496/1998: 130

The vessels-enhanced image is scaled and added to the original image so the blood vessels can be highlighted via their intensity with a volume-rendering opacity transfer function.

Other important structural components and landmarks, such as the ventricles, cortex, and skull, are visualized by increasing the volume rendering opacity by the local image gradient magnitude.

The tumor is segmented by first applying an edge-preserving smoothing filter, gradient-based anisotropic smoothing. This prevents leaking of a threshold-based region growing segmentation. The masked tumor is then added to the vessel-enhanced image at a different intensity magnitude so it can be highlighted in the opacity transfer function.

Generated with Jupyter, NiBabel, ITK, and itk-jupyter-widgets. Data from McGill-MNI, Rivaz, H., Chen, S, Collins, DL., Automatic Deformable MR-Ultrasound Registration for Image-Guided Neurosurgery, IEEE Trans. Medical Imaging, 2015, 34(2): 366–380.


**Code and data:** `1 <https://drive.google.com/open?id=1rqZ2lLb03oDnkHkNVPBcC_vaQw3enDhC>`__

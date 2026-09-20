<h2>TensorFlow-FlexUNet-Image-Segmentation-Multi-Organ-Gynaecological-MRI (2026/09/21)</h2>
Sarah T. Arai<br>
Software Laboratory antillia.com<br><br>
This is the first experiment in Image Segmentation for 
<b>Multi-Organ Gynaecological Magnetic Resonance Imaging for Brachytherapy-based Oncology
 (MOGaMBO)</b> 
based on our 
<a href="https://github.com/sarah-antillia/TensorFlow-FlexUNet-Image-Segmentation-Model"><b>TensorFlowFlexUNet Model</b></a> 
(TensorFlow Flexible UNet Image Segmentation Model for Multiclass), 
and a 512x512-pixel PNG 
<a href="https://drive.google.com/file/d/1-120uctQ3n5cPsBOxWsRiWeW5FMMnLGR/view?usp=sharing">
<b>MOGaMBO-ImageMask-Dataset.zip</b></a> with colorized masks 
(<a href="<a href="https://creativecommons.org/licenses/by/4.0/">CC BY 4.0</a>), 
which was derived by us from the Zenodo website<br><br>
<a href="https://zenodo.org/records/15156638">
<b>Multi-Organ Gynaecological Magnetic Resonance Imaging for Brachytherapy-based Oncology</b>
</a>
<br><br>
<hr>
<b>Actual Image Segmentation for MOGaMBO Images </b><br>
As shown below, the inferred masks predicted by our segmentation model trained on the dataset appear similar 
to the ground truth masks except for the second case.<br><br>
<table >
<tr>
<th>Input: image</th>
<th>Mask (ground_truth)</th>
<th>Prediction: inferred_mask</th>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/MOGaMBO/mini_test/images/10001_22.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/MOGaMBO/mini_test/masks/10001_22.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/MOGaMBO/mini_test_output/10001_22.png" width="320" height="auto"></td>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/MOGaMBO/mini_test/images/10002_40.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/MOGaMBO/mini_test/masks/10002_40.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/MOGaMBO/mini_test_output/10002_40.png" width="320" height="auto"></td>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/MOGaMBO/mini_test/images/10070_23.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/MOGaMBO/mini_test/masks/10070_23.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/MOGaMBO/mini_test_output/10070_23.png" width="320" height="auto"></td>
</tr>
</table>
<hr>
We used the following class_color_mapping table to generate our PNG dataset from the orginal NIfTI dataset.<br><br>
<b>class_color_mapping_table</b><br><br>
<table border=1 style='border-collapse:collapse;' cellpadding='5'>
<tr><th>Indexed Color</th><th>Color</th><th>RGB</th><th>Class</th></tr>
<tr><td>1</td><td with='80' height='auto'><img src='./color_class_mapping/S3.png' widith='40' height='25'></td>
<td>(255, 0, 0)</td><td>Bladder</td></tr>
<tr><td>2</td><td width='80' height='auto'><img src='./color_class_mapping/S1.png' width='40' height='25'></td>
<td>(0, 255, 0)</td><td>Rectum</td></tr>
<tr><td>3</td><td with='80' height='auto'><img src='./color_class_mapping/S2.png' widith='40' height='25'></td>
<td>(0, 0, 255)</td><td>Sigmoid Colon</td></tr>
<tr><td>4</td><td width='80' height='auto'><img src='./color_class_mapping/S4.png' width='40' height='25'></td>
<td>(255, 255, 0)</td><td>Femoral Heads</td></tr>
</table>
<br>
<h3>1.  Dataset Citation</h3>
The dataset used here was derived from <br><br>
<a href="https://zenodo.org/records/15156638">
<b>Multi-Organ Gynaecological Magnetic Resonance Imaging for Brachytherapy-based Oncology</b>
</a>
<br><br>
Das, Suresh (Annotator), Manna, Siladittya (Researcher), Ghosh, Sayantari (Supervisor)<br>
Bhattacharya, Saumik (Supervisor)
<br><br>
The following explanation (excerpt) was taken from the website above.<br><br>
<b>Description</b><br>
This dataset introduces a <b>Multi-Organ Gynaecological Magnetic Resonance Imaging for Brachytherapy-based Oncology
 (MOGaMBO)</b> dataset, a novel magnetic resonance imaging dataset aimed at advancing research in applications of 
 computational intelligence in brachytherapy diagnosis and organ segmentation for cervical cancer treatment. <br>
 The dataset comprises high-resolution T2-weighted 3D MR scans from 94 patients with locally advanced cervical cancer 
 (stages IB2–IVA), adhering to FIGO guidelines for interstitial and intra-cavitary brachytherapy. <br>
 The imaging was performed using a 1.5T GE Signa Explorer scanner, with acquisition parameters TR and TE set to 
 optimal values for soft-tissue contrast at 2600ms and 155ms, respectively, combined with a pixel 
 resolution of 0.5 × 0.5 mm² and 30–50 slices per scan. To ensure dosimetric consistency, bladder volume 
 was standardized via Foley catheterization during imaging. <br><br>
The <b>critical organs-at-risk—urinary</b> <br>
<b>bladder</b>, <br>
<b>rectum</b>, <br>
<b>sigmoid colon</b>, and<br>
<b>femoral heads</b>, <br>
were manually contoured by expert radiation oncologists using the open-source ITK-SNAP platform, 
 ensuring precise region-of-interest annotations. <br>
 The dataset underwent rigorous deidentification to protect patient privacy, removing all demographic 
 and identifiable information. MOGaMBO provides a standardized, privacy-compliant resource for developing 
 and validating medical image segmentation or representation learning algorithms, and brachytherapy-related 
 research tools. This dataset addresses a critical gap in accessible, multi-organ imaging resources for 
 the gynaecological brachytherapy dataset, with applications in treatment planning and AI-driven clinical research.
<br><br>
<b>Citation</b><br>
BibTex:<br>
<pre>
@misc{manna2025,
      title={Federated Self-Supervised Learning for One-Shot Cross-Modal and Cross-Imaging Technique Segmentation}, 
      author={Siladittya Manna and Suresh Das and Sayantari Ghosh and Saumik Bhattacharya},
      year={2025},
      eprint={2503.23507},
      archivePrefix={arXiv},
      primaryClass={cs.CV},
      url={https://arxiv.org/abs/2503.23507}, 
}
</pre>
<br>
<b>License</b><br>
<a href="https://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International</a>
<br><br>

<h3>
2. MOGaMBO ImageMask Dataset
</h3>
 If you would like to train this MOGaMBO Segmentation model,
please down load our dataset <a href="https://drive.google.com/file/d/1-120uctQ3n5cPsBOxWsRiWeW5FMMnLGR/view?usp=sharing">
<b>MOGaMBO-ImageMask-Dataset.zip</b> (<a href="<a href="https://creativecommons.org/licenses/by/4.0/">CC BY 4.0</a>)
</a> on Google Drive.
Expand the downloaded and put it under <b>./dataset/</b> to be:
<pre>
./dataset
└─MOGaMBO
    ├─test
    │   ├─images
    │   └─masks
    ├─train
    │   ├─images
    │   └─masks
    └─valid
         ├─images
         └─masks
</pre>
<br>
<b>MOGaMBO Statistics</b><br>
<img src ="./projects/TensorFlowFlexUNet/MOGaMBO/MOGaMBO_Statistics.png" width="512" height="auto"><br>
<br>
As shown above, the number of images of train and valid datasets is large enough to use as the training set for our segmentation model.
<br><br>
<b>Train_sample images</b><br>
<img src="./projects/TensorFlowFlexUNet/MOGaMBO/asset/train_images_sample.png" width="1024" height="auto">
<br>
<b>Train_sample masks</b><br>
<img src="./projects/TensorFlowFlexUNet/MOGaMBO/asset/train_masks_sample.png" width="1024" height="auto">
<br>
<h3>
3. Train TensorFlowFlexUNet Model
</h3>
 We trained the MOGaMBO TensorFlowFlexUNet Model by using the 
<a href="./projects/TensorFlowFlexUNet/MOGaMBO/train_eval_infer.config"> <b>train_eval_infer.config</b></a> file. <br>
Please move to the <b>./projects/TensorFlowFlexUNet/MOGaMBO</b> folder and run the following bat file.<br>
<pre>
>1.train.bat
</pre>
This simply runs the following command.<br>
<pre>
>python ../../../src/TensorFlowFlexUNetTrainer.py ./train_eval_infer.config
</pre>
<hr>

<b>Model parameters</b><br>
Defined a small <b>base_filters=16</b> and a large <b>base_kernels=(11,11)</b> for the first Conv Layer of Encoder Block of 
<a href="./src/TensorFlowFlexUNet.py">TensorFlowFlexUNet.py</a> 
and a large <b>num_layers=8</b> (including a bridge between Encoder and Decoder Blocks).
<pre>
[model]
image_width    = 512
image_height   = 512
image_channels = 3
input_normalize = True
normalization  = False
num_classes    = 5
base_filters   = 16
base_kernels  = (11,11)
num_layers    = 8
dropout_rate   = 0.05
dilation       = (1,1)
</pre>
<b>Learning rate</b><br>
Defined a small learning rate.  
<pre>
[model]
learning_rate  = 0.00007
</pre>
<b>Loss and metrics functions</b><br>
Specified "categorical_crossentropy" and "dice_coef_multiclass".<br>
<pre>
[model]
loss           = "categorical_crossentropy"
metrics        = ["dice_coef_multiclass"]
</pre>
<b >Learning rate reducer callback</b><br>
Enabled the learning_rate_reducer callback and a small reducer_patience.
<pre> 
[train]
learning_rate_reducer = True
reducer_factor     = 0.4
reducer_patience   = 4
</pre>
<b>Early stopping callback</b><br>
Enabled early stopping callback with the patience parameter.
<pre>
[train]
patience      = 10
</pre>
<b></b><br>
<b>RGB color map</b><br>
RGB color map dict for MOGaMBO 1+8 classes.<br>
<pre>
mask_datatyoe    = "categorized"
mask_file_format = ".png"
;MOGaMBO 1+4
; Bladder: blue
; Rectum:  green
; Sigmoid colon: red  
; Femoral heads: cyan
rgb_map= {(0,0,0):0,(0,0,255):1,(0,255,0):2,(255,0,0):3,(0,255,255):4}
</pre>
<b>Epoch change inference callbacks</b><br>
Enabled epoch_change_infer callback.<br>
<pre>
[train]
epoch_change_infer     = True
epoch_change_infer_dir =  "./epoch_change_infer"
epoch_change_tiled_infer     = False
epoch_change_tiled_infer_dir =  "./epoch_change_tiled_infer"
</pre>
By using this epoch_change_infer callback, on every epoch change, the inference procedure can be called
 for 6 images in <b>mini_test</b> folder. This will help you confirm how the predicted mask changes 
 at each epoch during your training process.<br> <br> 
<b>Epoch_change_inference output at starting (1,2,3)</b><br>
<img src="./projects/TensorFlowFlexUNet/MOGaMBO/asset/epoch_change_infer_at_start.png" width="1024" height="auto"><br>
<br>
<b>Epoch_change_inference output at middlepoint (14,15,16)</b><br>
<img src="./projects/TensorFlowFlexUNet/MOGaMBO/asset/epoch_change_infer_at_middle.png" width="1024" height="auto"><br>
<br>
<b>Epoch_change_inference output at ending (29,30,31)</b><br>
<img src="./projects/TensorFlowFlexUNet/MOGaMBO/asset/epoch_change_infer_at_end.png" width="1024" height="auto"><br>

<br>
In this experiment, the training process was stopped at epoch 31 by EarlyStoppingCallback.<br><br>
<img src="./projects/TensorFlowFlexUNet/MOGaMBO/asset/train_console_output_at_epoch31.png" width="1024" height="auto"><br>
<br>
<a href="./projects/TensorFlowFlexUNet/MOGaMBO/eval/train_metrics.csv">train_metrics.csv</a><br>
<img src="./projects/TensorFlowFlexUNet/MOGaMBO/eval/train_metrics.png" width="520" height="auto"><br>

<br>
<a href="./projects/TensorFlowFlexUNet/MOGaMBO/eval/train_losses.csv">train_losses.csv</a><br>
<img src="./projects/TensorFlowFlexUNet/MOGaMBO/eval/train_losses.png" width="520" height="auto"><br>
<br>
<h3>4. Evaluation</h3>
Please move to  <b>./projects/TensorFlowFlexUNet/MOGaMBO</b> folder, 
and run the following bat file to evaluate the TensorFlowFlexUNet model for MOGaMBO.<br>
<pre>
>./2.evaluate.bat
</pre>
This simply runs the following command.
<pre>
>python ../../../src/TensorFlowFlexUNetEvaluator.py  ./train_eval_infer.config
</pre>
Evaluation console output:<br>
<img src="./projects/TensorFlowFlexUNet/MOGaMBO/asset/evaluate_console_output_at_epoch31.png" width="1024" height="auto">
<br><br>Image-Segmentation-MOGaMBO

<a href="./projects/TensorFlowFlexUNet/MOGaMBO/evaluation.csv">evaluation.csv</a><br>
The loss (categorical_crossentropy) to the  <b>MOGaMBO/test</b> was low, and dice_coef_multiclass was
high, as shown below.
<br>
<pre>
categorical_crossentropy,0.0134
dice_coef_multiclass,0.994
</pre>
<br>
<h3>5. Inference</h3>
Please move to the <b>./projects/TensorFlowFlexUNet/MOGaMBO</b> folder and run the following bat file to infer segmentation regions for images using the trained TensorFlowFlexUNet model for MOGaMBO.<br>
<pre>
>./3.infer.bat
</pre>
This simply runs the following command.
<pre>
>python ../../../src/TensorFlowFlexUNetInferencer.py ./train_eval_infer.config
</pre>
<hr>
<b>mini_test_images</b><br>
<img src="./projects/TensorFlowFlexUNet/MOGaMBO/asset/mini_test_images.png" width="1024" height="auto"><br>
<b>mini_test_mask(ground_truth)</b><br>
<img src="./projects/TensorFlowFlexUNet/MOGaMBO/asset/mini_test_masks.png" width="1024" height="auto"><br>
<hr>
<b>Inferred test masks</b><br>
<img src="./projects/TensorFlowFlexUNet/MOGaMBO/asset/mini_test_output.png" width="1024" height="auto"><br>
<br>
<hr>
<b>Enlarged images and masks for MOGaMBO  Images </b><br>
As shown below, the inferred masks predicted by our segmentation model trained on the dataset appear similar 
to the ground truth masks.
<br><br>
<table>
<tr>
<th>Input: image</th>
<th>Mask (ground_truth)</th>
<th>Prediction: inferred_mask</th>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/MOGaMBO/mini_test/images/10021_25.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/MOGaMBO/mini_test/masks/10021_25.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/MOGaMBO/mini_test_output/10021_25.png" width="320" height="auto"></td>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/MOGaMBO/mini_test/images/10037_98.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/MOGaMBO/mini_test/masks/10037_98.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/MOGaMBO/mini_test_output/10037_98.png" width="320" height="auto"></td>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/MOGaMBO/mini_test/images/10044_17.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/MOGaMBO/mini_test/masks/10044_17.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/MOGaMBO/mini_test_output/10044_17.png" width="320" height="auto"></td>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/MOGaMBO/mini_test/images/10055_78.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/MOGaMBO/mini_test/masks/10055_78.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/MOGaMBO/mini_test_output/10055_78.png" width="320" height="auto"></td>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/MOGaMBO/mini_test/images/10075_47.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/MOGaMBO/mini_test/masks/10075_47.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/MOGaMBO/mini_test_output/10075_47.png" width="320" height="auto"></td>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/MOGaMBO/mini_test/images/10093_30.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/MOGaMBO/mini_test/masks/10093_30.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/MOGaMBO/mini_test_output/10093_30.png" width="320" height="auto"></td>
</tr>
</table>
<hr>
<br>
<h3>
References
</h3>
<b>1. Bridging the gap toward automated analysis of female pelvic MRI</b><br>
Elodie Germani, Krystel Nyangoh-Timoh, John SH Baxter, Pierre Jannin<br>
<a href="https://hal.science/hal-05534766v1/file/abstract-iabm-egermani.pdf">
https://hal.science/hal-05534766v1/file/abstract-iabm-egermani.pdf
</a>
<br><br>
<b>2. TensorFlow-FlexUNet-Image-Segmentation-Model</b><br>
Toshiyuki Arai <br>
<a href="https://github.com/sarah-antillia/TensorFlow-FlexUNet-Image-Segmentation-Model">
https://github.com/sarah-antillia/TensorFlow-FlexUNet-Image-Segmentation-Model
</a>
<br>
<br>

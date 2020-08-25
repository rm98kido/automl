# Execution Guide

fuer ausfuehrlichere beispiele: 
'efficentdet/tutorial.ipynb'

`cd efficientdet`<br>
`python -m venv env`<br>
`source env/bin/activate`<br>
`pip install -r requirements.txt`
`pip install -U 'git+https://github.com/cocodataset/cocoapi.git#subdirectory=PythonAPI`<br>
> Das Netz wurde auf dem COCO2017 datensatz trainiert

`wget https://storage.googleapis.com/cloud-tpu-checkpoints/efficientdet-d0`<br>
`tar zxf efficientdet-d0.tar.gz` <br>
`rm -r efficientdet-d0/save_model` <br>

`python model_inspect.py --runmode=saved_model \`
`--model_name=efficientdet-d0 --ckpt_path=efficientdet-d0 \`
`--saved_model_dir=efficientdet-d0/save_model --hparams="image_size=1920x1280"`

`python model_inspect.py --runmode=saved_model_infer \`<br>
  `--saved_model_dir=efficientdet-d0/save_model \`<br>
  `--model_name=efficientdet-d0  --input_image=IMGPATH  \`<br>
  `--output_image_dir=IMGoUTPUTpATH \`<br>
  `--min_score_thresh=0.35  --max_boxes_to_draw=200`

# Training Guide


# Brain AutoML

This repository contains a list of AutoML related models and libraries.

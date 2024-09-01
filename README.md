## Installation and Setup

1. Setup the conda environment 
    ```
    conda create --name 6dInHandVid python==3.8.11
    conda activate 6dInHandVid
    conda install pytorch==1.10.1 torchvision==0.11.2 torchaudio==0.10.1 cudatoolkit=11.3 -c pytorch -c conda-forge
    pip install -r requirements.txt
    ```
    
2. Clone the Current Repo
    ```
   git clone <curr_repo>
   cd 6dInHandVid
   cd main
    ``` 

## Training
1. Depending on the dataset and output pose respresentation you intend to train on, set the `dataset` & `pose_representation` variables in 
the `config.py`.
2. Run the following script to start the training:
    ```
    CUDA_VISIBLE_DEVICES=0,1 python train.py --run_dir_name <run_name>
    ```
    To continue training from the last saved checkpoint use `--continue` argument in the above command.
3. The checkpoints are dumped after every ecoch in the 'output' folder of the base directory
4. Tensorboard logging is also available in the 'output' folder

## Demo
Run the follwing script:
    ```
    python demo.py 
    ```



    
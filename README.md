# Fact-Based Logical Reasoning
This is the code for the project "Fact-Based Logical Reasoning".



## Environment
(I've set the environment with the latest versions of following libraries)

- python
- pytorch
- dgl-cu110
- transformers
- tensorboardX
- spacy

## Datasets 

followoing datasets were used for this project

- Reclor
- logiQA

## Hyperparameters
following are the hyperparameters that are set:

- model_type roberta 
- model_name_or_path $MODEL_NAME 
- task_name $TASK_NAME 
- do_train 
- evaluate_during_training 
- do_test 
- do_lower_case 
- data_dir $RECLOR_DIR 
- max_seq_length 384 
- per_gpu_eval_batch_size 1   
- per_gpu_train_batch_size 1   
- gradient_accumulation_steps 24 
- learning_rate 5e-06 
- num_train_epochs 10.0  
- logging_steps 200 
- save_steps 200 
- adam_betas "(0.9, 0.98)" 
- adam_epsilon 1e-6 
- no_clip_grad_norm 
- warmup_proportion 0.1 
- weight_decay 0.01 


## How to run?

Run the following code in bash terminal/console:

```bash
bash scripts/run_roberta_large.sh
```


Can change the dataset directory in the scripts to run different tasks. For example, to run logiQA, set 

```BASH
RECLOR_DIR = logiQA_data
TASK_NAME = logiqa
```

The accuracies of the "FOCAL REASONER" model on the dev sets are stored in the folder "Checkpoints", with test results stored in "test_pred.npy"

## Program_files folder

Project related program files(running of program) are stored in this folder.

## Project_Snaps folder

Accuracy/Performance/Analysis graphs & project related screenshots are stored in this folder. 

## Wandb folder

Logs and summaries of various metrics, hyper-parameters, and the outputs from the training runs are stored in th e wandb folder.




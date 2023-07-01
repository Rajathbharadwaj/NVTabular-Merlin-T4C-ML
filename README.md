# NVTabular-Merlin-T4C-ML
1july 2023
1. # Define the sequential input module :    https://nvidia-merlin.github.io/Transformers4Rec/stable/pipeline.html   or https://github.com/chenjie04/LSPM/blob/master/data_preprocess.py      you can use any link to define sequential input module 
to make the input in sequencce, we can use the above method . we have to give inputs in sequence to the model, so we have to convert in sequence on the basis of timestamp, which means we can sort in acsdeding order on the basis of timestamp and then group by userid   

# to check the functionality of schema : https://github.com/NVIDIA-Merlin/Transformers4Rec/blob/f3c4d2a6e67747a80030475fd5cea3f5371c327c/merlin_standard_lib/schema/schema.py#L214 ... 
here nvidia explained the internal functionality to create schema 

# to check the preprocessing before creating schema: https://www.kaggle.com/code/theoviel/pretraining-with-merlin-s-transformers4rec

# my dataset : https://www.kaggle.com/datasets/garymk/movielens-25m-dataset

# feature aggregation:   https://dl.acm.org/doi/pdf/10.1145/3460231.3474255
may be we are doing some problem when we are combining movie id, user id and genre together
I n order to achieve this the embeddings of item id and all additional features must share the same dimension. In our library we
support the element-wise merge approach proposed by [4], which
adds 1 to the resulting summation of additional features embeddings. As those embeddings are randomly initialized by 0-mean

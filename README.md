This work was done as a part of my master's thesis at Texas A&M. As AI models grow in size and complexity the resource demands are also growing. Sparse
inference is an approach to take advantage of sparsity in large AI models to make them run faster
thereby lowering the resource requirements. SuiteSparse:GraphBLAS, an open-source implementation of GraphBLAS, offers a robust framework tailored for leveraging sparsity in matrix computations. This work explores the application of SuiteSparse:GraphBLAS in performing inference tasks, particularly focusing on the language model BERT.
This work implements a complete inference pipeline using SuiteSparse:GraphBLAS. [Click here for a demo](https://colab.research.google.com/drive/13YwlILu4FNA2aXbTF86T991XAZYorsBq?usp=sharing)

The inference engine and the semi-ring formualtion of LLM inference can be found in the file [modeling_bert.py](https://github.com/deepaksuresh/transformers/blob/main/src/transformers/models/bert/modeling_bert.py). We start with the transformer implementation of BERT
inference and replicate that in SuiteSparse:GraphBLAS. The input preprocessing and output post-
processing are left untouched, focusing solely on the core inference process without altering the
surrounding setup.

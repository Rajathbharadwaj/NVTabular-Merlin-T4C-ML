# NVTabular-Merlin-T4C-ML

# How to make it work?

[Edit in this](https://github.com/NVIDIA-Merlin/Transformers4Rec/blob/f3c4d2a6e67747a80030475fd5cea3f5371c327c/transformers4rec/torch/features/tabular.py#L179) 

```python
 
maybe_categorical_module = cls.EMBEDDING_MODULE_CLASS.from_schema(schema, max_sequence_length=max_sequence_length,tags=categorical_tags, **kwargs
            )
```

But you have to do it in the local installation of your PC, typically it'll be at 

```
usr/local/lib/python3.8/dist-packages/transformers4rec/torch/features/tabular.py

```
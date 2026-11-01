# medora-models

ONNX **int8** (dynamic, per-channel) exports of open-source models, used by
[Medora](https://github.com/wajihtba) for in-process retrieval with ONNX Runtime.
Files are in the [Releases](../../releases); each `<model>.tar` extracts to `<model>/`
(`model.onnx`, `tokenizer.json`, configs). `models.sha256` lists every file's checksum,
`tars.sha256` the archives'.

| Archive | Upstream model | Licence | Role |
|---|---|---|---|
| `bge-m3-int8.tar` | [BAAI/bge-m3](https://huggingface.co/BAAI/bge-m3) | MIT | embedder (production) |
| `bge-reranker-v2-m3-int8.tar` | [BAAI/bge-reranker-v2-m3](https://huggingface.co/BAAI/bge-reranker-v2-m3) | Apache-2.0 | reranker (production) |
| `mmarco-mMiniLMv2-L12-H384-int8.tar` | [cross-encoder/mmarco-mMiniLMv2-L12-H384-v1](https://huggingface.co/cross-encoder/mmarco-mMiniLMv2-L12-H384-v1) | Apache-2.0 | optional fast reranker |
| `gte-multilingual-reranker-base-int8.tar` | [Alibaba-NLP/gte-multilingual-reranker-base](https://huggingface.co/Alibaba-NLP/gte-multilingual-reranker-base) | Apache-2.0 | optional reranker |
| `jina-reranker-v2-base-multilingual-int8.tar` | [jinaai/jina-reranker-v2-base-multilingual](https://huggingface.co/jinaai/jina-reranker-v2-base-multilingual) | CC-BY-NC-4.0 (non-commercial) | optional reranker |

These are derivative works (format conversion and int8 quantization only, no
retraining) distributed under each upstream model's licence; all credit to the
original authors. The upstream revision of each export is in its `revision` file.

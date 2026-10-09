# ZZB auxiliary weights

PyTorch checkpoints (`.pt`) and TensorRT engines (`.engine`) collected from
the same upstream sources as the main model store.

**ZZB does not load these directly.** The application scans `bin/models` for
`*.onnx` only, so nothing here appears in the in-app store. They are kept for
conversion and re-export:

    yolo export model=weights/<file>.pt format=onnx dynamic=true simplify=true

`weights.json` lists every file with its source repository.

Main model repository: https://github.com/MTxiaol/zzb-models
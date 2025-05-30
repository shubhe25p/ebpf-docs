---
title: "KFunc 'bpf_cpumask_any_and_distribute'"
description: "This page documents the 'bpf_cpumask_any_and_distribute' eBPF kfunc, including its definition, usage, program types that can use it, and examples."
---
# KFunc `bpf_cpumask_any_and_distribute`

<!-- [FEATURE_TAG](bpf_cpumask_any_and_distribute) -->
[:octicons-tag-24: v6.5](https://github.com/torvalds/linux/commit/f983be917332ea5e03f689e12c6668be48cb4cfe)
<!-- [/FEATURE_TAG] -->

Return a random set CPU from the AND of two CPU-masks.

## Definition

`src1`: The first CPU-mask.
`src2`: The second CPU-mask.

Return:
* A random set bit within [0, `num_cpus`) from the AND of two CPU-mask, if at
  least one bit is set.
* >= `num_cpus` if no bit is set.

`struct bpf_cpumask` pointers may be safely passed to `src1` and `src2`.

**Signature**

<!-- [KFUNC_DEF] -->
`#!c u32 bpf_cpumask_any_and_distribute(const struct cpumask *src1, const struct cpumask *src2)`
<!-- [/KFUNC_DEF] -->

## Usage

!!! example "Docs could be improved"
    This part of the docs is incomplete, contributions are very welcome

### Program types

The following program types can make use of this kfunc:

<!-- [KFUNC_PROG_REF] -->
- [`BPF_PROG_TYPE_LSM`](../program-type/BPF_PROG_TYPE_LSM.md)
- [`BPF_PROG_TYPE_PERF_EVENT`](../program-type/BPF_PROG_TYPE_PERF_EVENT.md) [:octicons-tag-24: v6.12](https://github.com/torvalds/linux/commit/bc638d8cb5be813d4eeb9f63cce52caaa18f3960) - 
- [`BPF_PROG_TYPE_STRUCT_OPS`](../program-type/BPF_PROG_TYPE_STRUCT_OPS.md)
- [`BPF_PROG_TYPE_TRACEPOINT`](../program-type/BPF_PROG_TYPE_TRACEPOINT.md) [:octicons-tag-24: v6.12](https://github.com/torvalds/linux/commit/bc638d8cb5be813d4eeb9f63cce52caaa18f3960) - 
- [`BPF_PROG_TYPE_TRACING`](../program-type/BPF_PROG_TYPE_TRACING.md)
<!-- [/KFUNC_PROG_REF] -->

### Example

!!! example "Docs could be improved"
    This part of the docs is incomplete, contributions are very welcome


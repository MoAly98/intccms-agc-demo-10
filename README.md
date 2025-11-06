# AGC Demo - CMS Analysis Integration Challenge

This repository demonstrates a complete CMS physics analysis workflow using Coffea and Dask for distributed computing.

## Prerequisites

Before running the notebooks, install `omegaconf`:

```bash
pip install omegaconf
```

## Repository Structure

```
.
├── example_cms/          # Example CMS analysis configuration
│   ├── configs/          # Analysis configuration (cuts, observables, systematics)
│   ├── corrections/      # Correction factors and calibrations
│   ├── datasets/         # Dataset definitions and queries
│   └── outputs/          # Analysis outputs (histograms, metadata)
├── src/intccms/          # Integration challenge CMS package
│   └── metrics/          # Performance monitoring and input inspection tools
├── full_run.ipynb        # Complete processor-based workflow demo
├── input_inspector.ipynb # ROOT file inspection and characterization
└── process_with_metrics.ipynb  # Workflow with comprehensive metrics collection
```

## Notebooks

### `full_run.ipynb`
Complete processor-based workflow:
- Configuration setup and metadata extraction
- Analysis execution with Coffea processor
- Histogram generation and statistical analysis

### `input_inspector.ipynb`
ROOT file characterization tools:
- Extract metadata (events, file sizes, branch properties)
- Distributed inspection using Dask
- Visualize data characteristics and compression ratios

### `process_with_metrics.ipynb`
Full workflow with performance monitoring:
- All features from `full_run.ipynb`
- Comprehensive metrics collection (throughput, resource usage)
- Worker tracking and performance visualization

## Output

Results are saved to `example_cms/outputs/`:
- `histograms/`: Analysis histograms in pickle and ROOT formats
- `metadata/`: Dataset metadata and file information
- `benchmarks/`: Performance metrics and tracking data (when enabled)

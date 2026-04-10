# AGENTS.md

## Project overview
This repository contains GROMACS workflows for fluorine-free CO2 thickener systems.
The main goals are:
1. build and organize simulation inputs,
2. automate trajectory analysis,
3. generate reproducible figures and summary tables for papers.

## Working rules
- Do not delete or overwrite raw input files in `systems/`, `mdp/`, or `topologies/`.
- Prefer adding new scripts under `scripts/` or `analysis/` instead of editing old scripts destructively.
- When changing any force-field-related file, explain the reason in the commit message or PR description.
- Keep all analysis reusable and batch-friendly.
- When generating figures, save them under `results/figures/`.
- When generating tables, save them under `results/tables/`.
- Use clear file names and avoid creating duplicate scripts with vague names like `final2.py`.

## Scientific checks
- Verify units carefully.
- Distinguish clearly between input structure files and output structure files.
- Do not modify molecular parameters silently.
- Flag any changes that affect thermostat, barostat, cutoffs, timestep, temperature, or pressure settings.
- For viscosity-related work, prefer relative comparison and descriptor analysis before expensive full validation.

## Review guidelines
- Check whether the workflow is reproducible from raw inputs.
- Check whether file paths are hard-coded.
- Check whether analysis scripts work for batch processing.
- Check whether figure labels and legends are publication-ready.
- Check whether changes may alter scientific interpretation, not only code style.

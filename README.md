# A prototype for Global Muon Tracks in ALICE/O2

This repository contains a prototype for global muon tracking for ALICE/O2. Some tools to study global muon tracking are also present.

`matcher.sh` automates the generation, matching and checking steps. See `matcher.sh --help`.


## 1. Generate compatible MCH and MFT Tracks

MCH tracks are created by simulations using aliroot. A configurable generator is found on `gen`. Convertion of MCH tracks to a transitional format to be read by O2 is done via macro `ConvertMCHESDTracks.C`.

MFT tracks are generated by the same kinematics file using `o2-sim`.


## 2. MCH-MFT Track Matching

MCH-MFT track matching and Global Muon Tracking is performed with class `MuonMatching` as implemented on `runMatching.C`.

## 3. Global muon tracks assesment

Macro `GlobalMuonChecks.C` can be used to check tracking. Histograms saved to `GlobalMuonChecks.root`
## Basic Configuration

* Place OCDB from https://gitlab.cern.ch/alisw/AliRootOCDB.git at `$HOME/OCDB`
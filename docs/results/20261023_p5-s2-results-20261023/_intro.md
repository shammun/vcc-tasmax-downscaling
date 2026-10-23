# AI downscaling (P5, S2): results in brief

**Headlines (draft)**

- **U-Net anomaly model vs v4.1.1, validation 2010-2014:** 0.648 C vs 0.7725 C RMSE; the U-Net anomaly model was not test-evaluated.
- **Test 3a (warmth test):** all 5 methods WARM-ROBUST on all days.
- **Spread calibration:** NOT CALIBRATABLE (flow matching, CorrDiff), although CRPS improves 7-11 % on validation.
- **Limitation:** inputs are coarsened PRISM (perfect prognosis), not GCM output; DWC reuses v4.1.1's own warming increment, so trend passes are agreement with v4.1.1, not independent skill.


- **Your first U-Net (anomaly, 18 Oct)** is as good as the later U-Nets on validation 2010-2014: RMSE 0.648 C raw, 0.648 C with de-warmed conditioning (DWC), vs 0.773 C for v4.1.1 (F1).
- It was **never scored on the test years 2015-2024**: only one U-Net (R1) entered the one-time test, so no test number exists for it.
- Fed raw warming inputs, every AI method distorted the future warming pattern (P3 FAIL, e.g. +0.60 C); with DWC all pass (F2).
- One-time test (5 methods): U-Net R1 -14.6 % RMSE vs v4.1.1 (SUCCESS-F); flow matching -20.8 %, CorrDiff -16.5 % (SUCCESS-P); EDM no gain; EnScale harmful (F3).
- The gain shrinks every year: U-Net -17.1 % in 2015 to -9.7 % in 2024; warmer days explain only a small part of this (F4).
- Ensemble spread of flow matching and CorrDiff is too narrow and a simple inflation cannot fix it exactly (F5).
- Limits: inputs are coarsened PRISM (perfect prognosis), not GCM output; DWC reuses v4.1.1's own warming increment, so the trend pass is agreement with v4.1.1, not independent skill; all deterministic gains share one U-Net backbone (one result).

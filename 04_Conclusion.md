---
title: Conclusion
numbering:
  enumerator: 4.%s
---

Optimizing SEM imaging for high-throughput data acquisition requires a careful balance between dwell time and pixel size to achieve both efficiency and accuracy in defect characterization.
This study demonstrates that acquisition times can be significantly reduced while preserving critical defect information by systematically adjusting these parameters.
A Python-based framework for automated defect detection was developed to analyze microstructural features in additively manufactured (AM) steel samples, leveraging local contrast conditions to enhance feature identification and ensure robustness across varying imaging conditions.

The findings highlight how pixel size and dwell time directly influence image quality, affecting accuracy in feature, e.g. defect, detection.
Pixel size determines the smallest detectable features, with smaller pixel sizes providing higher spatial resolution at the cost of longer acquisition times, while larger pixel sizes reduce resolution but accelerate data collection.
Increasing pixel size from 48 nm to 390 nm results in a substantial reduction in the number of detected defects, particularly in the sub- 5 µm² range, due to intensity averaging effects that obscure smaller features and distort defect dimensions.

Shorter dwell times improve acquisition speed but introduce more noise, obscuring fine details and reducing defect detection accuracy [@4].
A reduction in dwell time from 10 µs to 100 ns leads to a 43% decline in PSNR, reflecting the increased impact of noise on imaging quality.
To mitigate the influence of noise-induced artifacts, filtering constraints were introduced based on the observed PSNR trend, filtering out artificially features that result from excessive noise at lower dwell times.
Despite this correction, Area Adjusted Agreement (AAA) decreases sharply when both dwell time is reduced and pixel size is increased simultaneously, indicating a greater discrepancy between acquired images and the benchmark.
At shorter dwell times, defects become less distinct due to increased noise, while at larger pixel sizes, small defects are undetectable due to lower image resolution.
However, the increased noise from lower dwell times seems to have a more significant impact on the AAA values than the loss of resolution from an increase in pixel size.

Additionally, key defect descriptors such as roundness and orientation are affected by both parameters.
At longer dwell times and smaller pixel sizes, defect shapes are well-defined, allowing for more precise measurements.
However, at shorter dwell times, noise distorts defect boundaries, artificially decreasing roundness values.
Larger pixel sizes further impact defect characterization by averaging intensity values, making elongated defects appear more circular and reducing the accuracy of orientation measurements.

These findings underscore the necessity of carefully balancing dwell time and pixel size to optimize high-throughput SEM acquisition, ensuring both efficient data collection and reliable defect characterization.
By systematically tuning these parameters, it is possible to significantly reduce acquisition times while maintaining accurate and meaningful defect analysis, providing a scalable approach for advanced microstructural characterization in AM and beyond.

# asj90-speech-demo
Interactive demos for ASJ 90th anniversary poster

## Demos

- Connected-tube speech synthesizer
- Vocal-tract estimation from recorded speech using LPC / PARCOR
- DTW-based speech recognition


## Article

T. Shinozaki and Y. Ohtani, "音声技術今昔物語：ボコーダーから大規模モデルまで"
(Speech Technology Then and Now: From Vocoders to Large-Scale Models),
Journal of the Acoustical Society of Japan (in Japanese), Vol. 83, No. 2 (2027).
The appendix of the article explains the principles behind these demos.

## Conventions for the acoustic tube and PARCOR coefficients

The demos follow the formulation in the article appendix (cf. J. D. Markel and A. H. Gray Jr., *Linear Prediction of Speech*, Springer, 1976):

- The vocal tract is drawn from the glottis (left) to the lips (right); junctions are numbered m = 1, ..., P from the **lips** toward the glottis.
- R_m = (S_m − S_{m−1}) / (S_m + S_{m−1}), where S_m is the cross-sectional area on the glottis side of junction m (reflection coefficient for pressure waves).
- The PARCOR coefficient is k_m = −R_m, with A(z) = 1 + a_1 z^−1 + ... + a_P z^−P. Lattice stage 1 is on the lip (output) side.
- Areas are recovered from the lips as S_m = S_{m−1} (1 − k_m) / (1 + k_m).
- One sample corresponds to a round trip over one tube section of length L, so fs = c / (2L).

## Authors

Takahiro Shinozaki (Institute of Science Tokyo)  
Yamato Ohtani (National Institute of Information and Communications Technology, NICT)

The web pages and demonstration software in this repository were created by the authors above.

## License

Source code in this repository is licensed under the MIT License.

Third-party images and other materials are subject to their respective licenses.
Please refer to the attribution or license information accompanying each material.

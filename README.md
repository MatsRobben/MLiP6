For the PlantTraits competition the files are labeled according to Table 1 in the report.


| **Method**                                               | **Val** | **LB**     |
|----------------------------------------------------------|---------|------------|
| (1) Mean targets                                         | 0.00    | -0.00211   |
| (2) Classify species → lookup table                      | -       | -0.21434   |
| (3) EfficientNetB0 (Image only)                          | 0.3275  | 0.17917    |
| (4) + Target augmentation with SD                        | 0.1829  | 0.17791    |
| (5) Tabular data                                         | 0.2335  | 0.08429    |
| (6) EffNet & Tabular (concat)                            | 0.43    | 0.22832    |
| (7) + Balanced sampling                                  | 0.5584  | 0.19892    |
| (8) + More Augmentation                                  | 0.4221  | 0.24119    |
| (9)    + Remove Batchnorm from head                      | 0.4366  | 0.27696    |
| (10)      + SmoothL1Loss                                 | 0.4290  | 0.26589    |
| (11)      + Multiple patches at test time                | -       | 0.28119    |
| (12)      + Log transform relevant tabular               | 0.4342  | 0.27189    |
| (13)      + Predict targets individually                 | 0.4175  | 0.24462    |
| (14)      + Remove less outliers                         | 0.4447  | 0.26428    |
| (15)      + Log transform relevant targets               | 0.4221  | 0.25780    |
| (16) Swin Transformer (Image only)                       | 0.5582  | 0.35420    |
| (17) + All data (without val set)                        | -       | 0.37687    |
| (18)    + Concat with Tabular                            | -       | 0.38428    |
| (19)    + SmoothL1Loss                                   | -       | 0.41001    |
| (20)      + SwinV2                                       | -       | 0.36319    |
| (21)      + More Augmentation                            | -       | 0.39900    |
| (22)      + Multiple RandomCrop during test              |         | 0.41072    |
| (23) XGBoost: Swin features & Tabular                    | 0.61995 | 0.38763    |
| **Ensembles:**                                           |         |            |
| (24) XGBoost & Swin&Tabular                              | -       | 0.42586    |
| (25) + Swin (Only images)                                | -       | 0.43360    |
| (26) + All data for Swin&Tabular                         | -       | 0.44049    |
| (27) + Swin&Tabular: more augmentation                   | -       | 0.44585    |
| (28) + RandomCrop during test                            | -       | 0.44684    |

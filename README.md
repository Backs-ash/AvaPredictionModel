# AvaPredictionModel

AvaPredict is a neural network that utilises past spatial data around multiple
sub-sections, analyses variables and outputs the possible geo-location and the
probability of an avalanche occuring in and around that location. The model is
<ins>xxx%</ins> accurate based on the training and testing data provided to it.
The model will be used in tandem with the
[real-time data collection radar based system](https://github.com/Backs-ash/RadarBasedAvaPredict).
RadarBasedAva will verify the outputs given by AvaPredict to make a redundant
system for the user.

### Datasets utilised

---

We have extracted data from <ins>so and so</ins> resources. The data is divided
into two parts namely - (i) Training group (ii) Testing group

### Proposed pipeline

---

We can predict the data based on the below factors -

- Topographic Position Index (TPI)
- Topographic Ruggedness Index (TRI)
- Topographic Wetness Index (TWI)
- Vector Ruggedness Measure (VRM)
- Wind Exposition Index (WEI)
- Relative Slope Position (RSP)
- Lithology
- Length-Slope (LS)
- Slope degree
- Distance from Streams
- Profile Curvature
- Aspect
- Elevation
- Land Use

More information about these factors can be found in the research conducted by
[Omid Rahmati et al.](https://www.mdpi.com/2072-4292/11/24/2995)

These predictive factors are then undergone through four different machine
learning(ml) models. Namely - Support Vector Machine(SVM), Random Foster (RF),
Naive Bayes (NB) and Generalised Additive Model (GAM).

The accuracy of these models is then compared to few well known models and the
goodness of the fit. Metrics like F1 (Precision x Recall / Precision + Recall),
Matthews correlation coefficient (MCC), AUROC, etc are being utilised by
[Omid Rahmati et al.](https://www.mdpi.com/2072-4292/11/24/2995) in their
reasearch about the prediction of geo-spatial occurance of an avalanche.

Their proposed models perform fairly well to be used by our eco-system. It was
also found that the LS of a region played the most prominent role relative to
other factors when an avalanche was predicted.

### Using the repository

---

The `data` folder contains all the necessary set-up for the training model(You
may find you data sources over here). The test runs for the model will provide
the output in this folder as well. <br> The `src` folder contains the source
files for the prposed four part machine learning model.

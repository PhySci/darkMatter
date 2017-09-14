# darkMatter
Dark Matter signal search. Episode 2.1
https://inclass.kaggle.com/c/dmse-2-1

## Find traces of electromagnetic showers that may be a signal of dark matter particles

The data sample comes from OPERA (http://operaweb.lngs.infn.it) experiment that is well-known to find neutrinos using photo emulsion technique. Neutrinos themselves are invisible in the detector, but a very small fraction of them will interact with material in the detector and produce an electromagnetic shower in case of a scattered electron and also a hadronic shower in case of a scattered nucleus. The goal of the machine learning competition is to find traces of electromagnetic showers within a very dense background sample (see figure). Atomic electrons can also be scattered by light dark matter which is searched for by other experiments, including those at CERN, for example at SHiP (http://ship.web.cern.ch), which is going to use very similar neutrino detection techniques as the OPERA experiment.

## Data fields in training/test sets

training/test samples

    Id - ID of a track
    X - X coordinate of the track start
    Y - Y coordinate of the track start
    Z - Z coordinate of the track start
    TX - angle of the track in XZ plane
    TY - angle of the track in YZ plane
    chi2 - goodness of fit of the track line to the track hits

there is signal field in the training set, which equals to 1.0 for signal event and to 0.0 otherwise.

Training set also has field event_id either equals to -999, which means this track is a background or equals to shower ID (like in Episode 1) in case it is signal.

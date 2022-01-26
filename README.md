# Stellar Classification

### In this project, it has been used different Machine Learning models to classify stars based on their spectral characteristics. The goal is to classify an object as a star, galaxy or quasar.

<p align="center"><img src="data/galaxy.gif" width="100%" height="100%"/></p>
<h6 align="center">Image obtained from <a href="https://sci.esa.int/web/hubble/-/hubble-surveys-gigantic-galaxy-heic2002">European Space Agency - ESA.</a></h6>
  
### Models implemented by <a href="https://github.com/AnneLivia">Anne Livia</a>.

## Dataset Information:

- fedesoriano. (January 2022). **Stellar Classification Dataset - SDSS17**. Retrieved [Date Retrieved] from <a href="https://www.kaggle.com/fedesoriano/stellar-classification-dataset-sdss17">this link</a> on Kaggle.

- ***"In astronomy, stellar classification is the classification of stars based on their spectral characteristics. The classification scheme of galaxies, quasars, and stars is one of the most fundamental in astronomy. The early cataloguing of stars and their distribution in the sky has led to the understanding that they make up our own galaxy and, following the distinction that Andromeda was a separate galaxy to our own, numerous galaxies began to be surveyed as more powerful telescopes were built. This datasat aims to classificate stars, galaxies, and quasars based on their spectral characteristics."*** - fedesoriano.

- The data consists of **100,000** observations of space taken by the SDSS (Sloan Digital Sky Survey). Every observation is described by 17 feature columns and 1 class column which identifies it to be either a **star, galaxy or quasar**.

### Properties:

  - **obj_ID** = Object Identifier, the unique value that identifies the object in the image catalog used by the CAS
  - **alpha** = Right Ascension angle (at J2000 epoch)
  - **delta** = Declination angle (at J2000 epoch)
  - **u** = Ultraviolet filter in the photometric system
  - **g** = Green filter in the photometric system
  - **r** = Red filter in the photometric system
  - **i** = Near Infrared filter in the photometric system
  - **z** = Infrared filter in the photometric system
  - **run_ID** = Run Number used to identify the specific scan
  - **rereun_ID** = Rerun Number to specify how the image was processed
  - **cam_col** = Camera column to identify the scanline within the run
  - **field_ID** = Field number to identify each field
  - **spec_obj_ID** = Unique ID used for optical spectroscopic objects (this means that 2 different observations with the same - spec_obj_ID must share the output class)
  - **class** = object class (galaxy, star or quasar object)
  - **redshift** = redshift value based on the increase in wavelength
  - **plate** = plate ID, identifies each plate in SDSS
  - **MJD** = Modified Julian Date, used to indicate when a given piece of SDSS data was taken
  - **fiber_ID** = fiber ID that identifies the fiber that pointed the light at the focal plane in each observation

# Software Information

  - Python
  - Pandas
  - Scikit-learn
  - Matplotlib
  - Seaborn
  - XGBoost

# Trained Models 

  - <h3>Decision Tree Model</h3>

                      precision    recall  f1-score   support

           0              0.98      0.99      0.98     11871
           1              1.00      1.00      1.00      4308
           2              0.96      0.93      0.94      3821
           
           accuracy                           0.98     20000
           macro avg      0.98      0.97      0.97     20000
           weighted avg   0.98      0.98      0.98     20000
   
  - <h3>Random Forest Model</h3>
  
                      precision    recall  f1-score   support

           0              0.98      0.99      0.98     11871
           1              0.99      1.00      1.00      4308
           2              0.97      0.94      0.95      3821

          accuracy                            0.98     20000
          macro avg       0.98      0.97      0.98     20000
          weighted avg    0.98      0.98      0.98     20000
    
  - <h3>Extra Tree Model</h3>

                      precision    recall  f1-score   support

           0              0.96      0.98      0.97     11871
           1              0.97      0.98      0.97      4308
           2              0.97      0.90      0.94      3821

          accuracy                            0.97     20000
          macro avg       0.97      0.95      0.96     20000
          weighted avg    0.97      0.97      0.97     20000
  
  - <h3>XGBoost model</h3>

                      precision    recall  f1-score   support

           0               0.98      0.99      0.98     11871
           1               1.00      1.00      1.00      4308
           2               0.96      0.94      0.95      3821

          accuracy                             0.98     20000
          macro avg        0.98      0.98      0.98     20000
          weighted avg     0.98      0.98      0.98     20000
  
  - <h3>AdaBoost model</h3>

                      precision    recall  f1-score   support

           0              0.75      0.93      0.83     11871
           1              0.98      1.00      0.99      4308
           2              0.11      0.03      0.04      3821

           accuracy                           0.77     20000
           macro avg      0.61      0.65      0.62     20000
           weighted avg   0.68      0.77      0.71     20000

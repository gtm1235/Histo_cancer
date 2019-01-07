# Histo_cancer
Kaggle competition for Cancer detection in histology slides

***Not Yet Deployable -- Still training for better accuracy***

Still working Kaggle Update is most recent with 86% at 70K tested .. model_checkpoint is present. following info for loading:
trained on gpu. Please note that I have not added any instruction to load as I am still fine tuning the project .. I t has turned out to be much more challenging to get the results over 90 percent than I imagined! however in my repositry there is a model uploaded and the parameters in the saved file are as below .. image is 224 x 224 and must be normalized with mean and standard deviation:

([0.485, 0.456, 0.406],
[0.229, 0.224, 0.225])])

TODO: write all functions after fine tuning model
TODO: write output to Pandas Dataframe
TODO: Annotate Notebook

checkpoint = {'batch_size': 64,
                      'valid_transforms': valid_transforms,
                      'train_transforms': train_transforms,
                      'model': model,
                      'classifier': fc,
                      'criterion': criterion,
                      'optimizer': optimizer.state_dict(),
                      'state_dict': model.state_dict()
                      }

I am working on the best model while manageing time constraints.

Ideally once a proper model of 97% or above is reached to turn the model into production using PyTorch 1.0. I envision a variety of models trained 
by cell type to more accurately detect cancer. There could be a chip based algorithm on microscopes in histology labs or a web based interface for 
uploading pictures.

I would also like to build a deployable app through Kiva (GUI) that would work on Windows, Apple, Linux, and Android devices.  

It may be possible to overlay a GUI using scorch and pytorch to produce a deployable model that anyone with a decent GPU could use. Imagine 
where you could add the file path for your data, click the radio boxes for transforms and models, Choose loss and optimizers and paramaters,
as well as build fc layers through a simple gui. all of the coding behind the screens. Progress updates could be printed for testing through 
eophcs, image number, graphs, validation loss, accuracy etc all available on screen.



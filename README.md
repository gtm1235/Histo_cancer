# Histo_cancer
Kaggle competition for Cancer detection in histology slides


Still working Kaggle Update is most recent with 86% at 70K tested .. model_checkpoint is present. following info for loading:
trained on gpu.

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



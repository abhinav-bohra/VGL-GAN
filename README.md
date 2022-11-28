#VGL-GAN
-----
Video Game Level Generation using Deep Convolutional Generative Adversarial Network

The project is derived from the *[/MarioGAN-LSI](https://github.com/icaros-usc/MarioGAN-LSI)* project. and *[Mario-AI-Framework](https://github.com/amidos2006/Mario-AI-Framework)* 

## Proposed Model Architecture
![Model-Design](https://github.com/abhinav-bohra/VGL-GAN/blob/main/Docs/Model.png)

## Generated Levels
![Model-Design](https://github.com/abhinav-bohra/VGL-GAN/blob/main/Docs/Levels.png)

## Getting Started

Download or clone this repository on your system.

### Prerequisites
```
- PYTHON 3.8.1
- JAVA 1.8.0
```

### Installing
- Install python3 on your system
- Add python to environment variables
- Navigate to 'CoeuSearch' folder in terminal 
- Create an evironment using the following command -> virtualenv CoeuSearch
- Activate the evironment using the following command  
```
     .\CoeuSearch\Scripts\activate    (For Windows)
      source CoeuSearch\bin\activate  (For Ubuntu)
```
- Run command ```pip3 install -r requirements.txt```
- Change ```cache_base_path``` in configs.py according to your machine path
- Run command ```python3 manage.py runserver```
- Click on localhost link generated after execution of previous command

## Training the GAN
The GAN that generates Mario levels can be run by the following command in the GANTrain folder:

```
python3 GANTraining.py --cuda
```

Pretrained model can be downloaded from *[MarioGAN-LSI-pretrained-model](https://github.com/icaros-usc/MarioGAN-LSI/blob/master/GANTrain/samples/netG_epoch_4999_7684.pth)* in the repo.

## Running LSI Experiments
Experiments can be run with the command:
```
python3 search/run_search.py -w 1 -c search/config/experiment/experiment.tml
```

The w parameter specifies a worker id which specifies which trial to run from a given experiment file. This allows for parallel execution of all trials on a high-performance cluster.

## Future Work
> - Extend this tool for other video games like DOOM and Lode Runner

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

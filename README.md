# data_version_control_tutorial


## Adicionando um repositório
```
git remote set-url origin git@github.com:rodneyrick/data_version_control_tutorial.git
git remote add origin git@github.com:rodneyrick/data_version_control_tutorial.git
```

## Instalação das libs básicas para estudo
```
pip install dvc scikit-learn scikit-image pandas numpy
```

## Criando o diretório de pastas e arquivos
```
mkdir {data,metrics,model,src}
mkdir {data/prepared,data/raw}
touch {src/prepare.py,src/train.py,src/evaluate.py}
```

## Download dataset
```
curl https://s3.amazonaws.com/fast-ai-imageclas/imagenette2-160.tgz -O imagenette2-160.tgz
tar -xzvf imagenette2-160.tgz
mv imagenette2-160/train data/raw/train
mv imagenette2-160/val data/raw/val
rm -rf imagenette2-160
rm imagenette2-160.tgz

https://www.kaggle.com/c/titanic/data?select=train.csv

mv train.csv data/raw/train/train.csv
mv test.csv data/raw/test/test.csv
```

# Practice the Basic DVC Workflow
```
git checkout -b "feature/first_experiment"
```
## Adicionando um versionamento local
dvc remote add -d myremote /tmp/dvcstore

## Tracking Files
```
dvc add data/raw/train
dvc add data/raw/val
```







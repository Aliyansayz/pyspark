# pyspark
developing pyspark applications best practices
VIDEO ----> https://www.youtube.com/watch?v=RAT-gQccsEs

Folder Structure:
| spark-python
  | .venv
  | dist
    --main.py
    --src.zip
  | src
    -- __init__.py
    -- welcome.py
  -- main.py
  -- Makefile
  
  
  
TASK 1 : SET UP VIRTUAL ENVIRONMENT

STEP 1 : 

set PIPENV_VENV_IN_PROJECT

STEP 2 :
PIPENV_VENV_IN_PROJECT = 1 pipenv shell


TASK 2 : INSTALL PYSPARK 

spark-python/  pipenv install pyspark 

_________________


TASK 3 : ADD MAKEFILE IN spark-python/

Step 1 :
( Makefile )
build :
    mkdir ./dist
    cp main.py
    cd ./src && zip  -r ../dist/src.zip . 
    
    
STEP 2 : 

spark-python/ make build

_____________________

TASK 4 : RUN SPARK CLUSTER

spark-python/ cd dist  &&  spark-submit --master local --py-files src.zip main.py && cd

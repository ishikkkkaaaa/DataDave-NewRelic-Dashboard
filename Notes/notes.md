> create an acc
> setup OS
> get your account ID + Licence key
> setup local env
> python should be - < 3.12
> better to use `pyen` (make sure u deactivate the env) -> 
    `brew install pyenv`
    instal python 3.10
    `pyenv install 3.10.13
    pyenv local 3.10.13`  #local for this directory
> recreate the env 
    `python3 -m venv venv
source venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt
`
Note - make sure you have python 3.10 installed. make sure you create a pyenv, install python 3.10
check version
>config .ini file `newrelic-admin generate-config NRAK-V5PTESLJTATU0IKP6FV9H7TIAZA newrelic.ini  `
>make sure path is correct, if no  `export NEW_RELIC_CONFIG_FILE=/Users/ishikakesarwani/Desktop/DataDaveChallenge_DevRel`
> change account id in both game.py and .ini file
> verify if youre able to access this file `cat $NEW_RELIC_CONFIG_FILE`
> to run the file `python game.py   `
> 


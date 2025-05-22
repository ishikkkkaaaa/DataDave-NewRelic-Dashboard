> create an acc
> setup OS
> get your account ID + Licence key
> setup local env
> python should be - < 3.10
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
>config .ini file `newrelic-admin generate-config License-key newrelic.ini  `
>make sure path is correct, if no  `export NEW_RELIC_CONFIG_FILE=/Users/ishikakesarwani/Desktop/DataDaveChallenge_DevRel`
> change account id in both game.py and .ini file
> verify if youre able to access this file `cat $NEW_RELIC_CONFIG_FILE`
> to run the file `python game.py   `
> 

----
datapoints
> items colelction - diamond, ruby, trophy, pink, gun
> deaths
> levels
> top score
> current score
> RAM
> date - time

> death vs score (bell curve)
> top score vs level (chart?)
> item collection dashboard - per level, mac number of ruby, trophy etc level (product pov)
> death against - how many items collected
> system level points - RAM usage (check python lib)
>
export NEW_RELIC_CONFIG_FILE=/Users/ishikakesarwani/Desktop/DataDaveChallenge_DevRel/newrelic.ini

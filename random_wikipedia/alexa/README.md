
# Create App and Add Requirements

python3 -m pip install --user virtualenv

python3 -m virtualenv env

source env/bin/activate

pip3 install -r requirements.txt -t .

#  Build and Push

zip -r9 ../function.zip .

cd ..

aws lambda update-function-code --function-name random_wikipedia --zip-file fileb://function.zip
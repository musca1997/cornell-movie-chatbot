

## Data Preparing

* Download raw data from Cornell Movie Corpus:
https://people.mpi-sws.org/~cristian/data/cornell_movie_dialogs_corpus.zip

* Unzip the file, and put it in prepare_data
```bash
cd prepare_data
python prepare_data.py
```

* Make a new directory named working_dir and data
```bash
cd cornell-movie-chatbot
mkdir working_dir
mkdir data
```

* put the output of prepare_data.py in data

## Training

```bash
# edit seq2seq.ini file to set
#		mode = train
python execute.py
# or use custom ini file
#		python execute.py my_custom_conf.ini
```

## Testing

```bash
# edit seq2seq.ini file to set
#		mode = test
python execute.py
```

## Serve

```bash
# configuration : seq2seq_serve.ini
python ui/app.py
# wait until this message shows up
#		"Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)"
# open up the address in browser, chat with the bot
```

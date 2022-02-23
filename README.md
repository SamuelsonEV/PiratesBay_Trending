# Trending torrents on PiratesBay

This Jupyter Notebook file access PiratesBay's torrent list (sorted by most leechers first) and store it on a pickle file, so later its possible to compare a new one to it and classify by the torrents on the list that changed most its position upwards the torrent list (most trending torrents to least trending).
Finnaly it presents the user with the resulting trending torrent list each with its own magnet link for the user's convenience.
* Notice that it compares the changes since last access, it only will have 2 Epoch's to compare on the second time it runs.
---
### Running it locally  on a **docker** container
1. Enter the repository folder than run:
```shell
docker run -i -t -v $(pwd):/home/jovyan  -p 8888:8888 --rm --name jupyterlab continuumio/anaconda3 /bin/bash -c "\
  conda install -c conda-forge jupyterlab -y --quiet && \
  conda install -c conda-forge nodejs -y --quiet && \
  conda install -c conda-forge/label/gcc7 nodejs -y --quiet && \
  conda install -c conda-forge/label/cf201901 nodejs -y --quiet && \
  conda install -c conda-forge/label/cf202003 nodejs -y --quiet && \
  jupyter lab  --ip='*' --port=8888  --no-browser --allow-root"
```
2. Access the link(containing the access token) that will appear when the last command finishes.
3. Finnaly access ```http://127.0.0.1:8888/lab/tree/home/jovyan/Piratesbay_trending.ipynb``` and run all cells.

---
### Running it on Google Colaboratory (Colab)
Upload it to ```https://colab.research.google.com/``` and run all cells.  

---
### Test it right now running on Heroku   
[TEST HERE](https://piratesbay-trending.herokuapp.com/app/1)

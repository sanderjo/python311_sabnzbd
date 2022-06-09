# docker-sabnzbd3-python3.9
Docker image with SABnzbd3 (from github) with python 3.11


# Build

docker build  -t="sabnzbd-py311" .

(Note the dot at the end)

Or brand new building (can take 5-10 minutes)

docker build --no-cache -t="sabnzbd-py311" .

# Run
docker run -p 8080:8080 --name sabnzbd-py311 sabnzbd-py311

# Kill
docker kill sabnzbd-py311

# Remove
docker rm sabnzbd-py311

# Output on stdout

```
$ docker run -p 8080:8080 --name sabnzbd-py311 sabnzbd-py311
2022-06-09 17:32:30,060::INFO::[SABnzbd:1167] --------------------------------
2022-06-09 17:32:30,060::INFO::[SABnzbd:1168] SABnzbd.py-3.7.0-develop
2022-06-09 17:32:30,108::INFO::[misc:1163] [sabnzbd.misc.run_command] Running external command: ['git', 'rev-parse', '--short', 'HEAD']
2022-06-09 17:32:30,109::DEBUG::[misc:1164] Popen arguments: {'stdin': -1, 'stdout': -1, 'stderr': -2, 'startupinfo': None, 'creationflags': 0, 'cwd': '/sabnzbd'}
2022-06-09 17:32:30,112::INFO::[SABnzbd:1364] Commit = fb75cde71
2022-06-09 17:32:30,112::INFO::[SABnzbd:1366] Full executable path = /sabnzbd/SABnzbd.py
2022-06-09 17:32:30,112::INFO::[SABnzbd:1367] Arguments = "/sabnzbd/SABnzbd.py" "-b0" "--server" "0.0.0.0:8080" "-l2"
2022-06-09 17:32:30,113::INFO::[SABnzbd:1368] Python-version = 3.11.0b3 (main, Jun  1 2022, 23:49:29) [GCC 11.2.0]

```
Note the python version: 3.11.x

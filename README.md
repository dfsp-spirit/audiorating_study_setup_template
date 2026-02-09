# audiorating_study_setup_template
A template repo with scripts that quickly allow you to deploy your [audiorating](https://github.com/dfsp-spirit/audio_rating) study. Clone it to create a study.


## About

This simple repo contains:

* directories into which to organize your study config file (studies_config.json) and your music files in wav or mp3 format.
* the script `deploy_study.sh` which will put the files into the correct place, given your audiorating installation path, and will also create the study live in the database

Note that the studies added to your server by running this script will NOT disable or in any other way affect existing studies, so you can run several scripts for different studies one after another on the same server. The only limitation is that they must not contain studies which use the same unique study name.

Together, this allows you to quickly deploy your study configurations on several machines (e.g., local development/testing laptop and staging or production server) in a reproducible way.


## Usage

* Clone this repo
* Put you files into audio_files/ directory in wav or mp3 format. Use filename without special characters, sticking to ASCII letters and numbers and the underscore only is safest, e.g. `my_great_song_from_2025.mp3`. Note that you CAN use special characters in the song description in the config file, which will be displayed as a song title to study participants. The file name will NOT be displayed to participants anyways, so there is no point in being getting too fancy here.
* Edit the config/studies_config.json file.
* Run the deploy_study.sh script


## Author and License

Created by [Tim Schäfer](https://github.com/dfsp-spirit/). Like audio_rating itself, and the wavesurfer.js library used by it, this repo is licensed under the very permissive [BSD 3-clause license](./LICENSE).

# image-study

Stable entry point for a research study run from a university compute cluster.

The study app itself is not hosted here — it runs behind a tunnel whose hostname can
change. This repo publishes one permanent URL:

    https://simran-khanuja.github.io/image-study/

`index.html` redirects there-to-here, forwarding the query string so the recruitment
platform's participant ID reaches the app. When the tunnel changes hostname, only the
`TARGET` line in `index.html` changes; every link already in a participant's hands
keeps working.

Update it from the study repo with:

    python human_study/serve/update_redirect.py --from-log --commit

No study data, stimuli, or participant responses are stored in this repository.

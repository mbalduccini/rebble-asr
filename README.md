# rebble-asr
asr.rebble.io: speech recognition for rebble

# Building
docker build --tag rebble-asr .

# Running
docker run --name rebble-asr -d --rm -e "PORT=443" -e "SPEECH_API_KEY=[api]" -e "MY_HTTP_REFERER=[HTTP referer]" -p 127.0.0.1:10041:443/tcp rebble-asr

[api] is the Google Cloud Speech-to-Text API key

[HTTP referer] is an HTTP referer authorized in the Google Cloud Speech-to-Text console for the API key

Optional command-line argument:

         -e "ALLOWED_PHONES=[list]"

[list] is a comma-separated list of allowed phones based on the user-agent information provided by the phone.

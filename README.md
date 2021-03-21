# rebble-asr
asr.rebble.io: speech recognition for rebble

# Building
docker build --tag rebble-asr .

# Running
docker run --name rebble-asr -e "PORT=443" -e "SPEECH_API_KEY=<api>" -p 127.0.0.1:10041:443/tcp rebble-asr


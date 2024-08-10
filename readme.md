1. 前端可以保存视频，直接live server即可
2. 后端通过 ffmpeg + node-media-server 来实现推流，前端使用flv.js来实现拉流
    推送视频：
        ffmpeg -re -i C:\Users\aywzc\Desktop\LiuYing.mp4 -c copy -f flv rtmp://localhost:1935/live/STREAM_NAME
    推送屏幕：(Error)
        ffmpeg -f avfoundation -i "1" -vcodec libx264 -preset ultrafast -acodec libfaac -f flv rtmp://localhost:1935/live/STREAM_NAME
npm i
node index.js
然后ffmpeg打开推流
前端使用live server即可

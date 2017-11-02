# slack-hubot-sample

## install software

$ sudo apt install nodejs

$ sudo apt install npm

$ npm install

$ . .envrc

## start sample

$ mkdir samplebot

$ cd samplebot

$ yo hubot

Please answer the question.

## edit samplebot/package.json

Add '"coffee-script": "~1.12.7"' for dependencies section.

## edit samplebot/external-scripts.json

Remove 'hubot-heroku-keepalive'.

Remove 'hubot-redis-brain'.    # とりあえず、Redis をインストールするまでの間は削除しとく

## Export

export HUBOT_SLACK_TOKEN=xoxb-XXXXXXXXX    # ボットのアクセストークン

## Run slack adapter

1. ボットを何らかのチャンネルに参加させる、もしくはチャンネルを作成しその時ボットを参加させる

2. cat samplebot/scripts/hello.js  
// Description:  
//   HelloWorld  
module.exports = function(robot) {  
        robot.send({room: "#channel-name"}, "Hello! World!");  
};  

3. コマンド実行  
./bin/hubot --adapter slack


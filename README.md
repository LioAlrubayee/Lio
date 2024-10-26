# Lio
Lio
<?php 
ob_start();
$token = "6038105517:AAGknwFqOe4vuZ0SmRto3WF6hHIqhbIg5Jw"; #token
define("API_KEY",$token);
echo file_get_contents("https://api.telegram.org/bot" . API_KEY . "/setwebhook?url=" . $_SERVER['SERVER_NAME'] . "" . $_SERVER['SCRIPT_NAME']);
function bot($method,$datas=[]){
$url = "https://api.telegram.org/bot".API_KEY."/".$method;
$ch = curl_init();
curl_setopt($ch,CURLOPT_URL,$url);
curl_setopt($ch,CURLOPT_RETURNTRANSFER,true);
curl_setopt($ch,CURLOPT_POSTFIELDS,$datas);
$res = curl_exec($ch);
if(curl_error($ch)){
var_dump(curl_error($ch));
}
else
{
return json_decode($res);}}

$update = json_decode(file_get_contents('php://input'));
$message = $update->message;
$message_id = $update->message->message_id;
$username = $message->from->username;
$title = $message->chat->title;
$text = $message->text;

@$re_id = $update->message->reply_to_message->from->id;
@$re_user = $update->message->reply_to_message->from->username;
@$re_name = $update->message->reply_to_message->from->first_name;
if($update->message){
$chat_id = $update->message->chat->id;
$title = $update->message->chat->title;
$message_id = $update->message->message_id;
$name = $update->message->chat->first_name;
$user = $update->message->chat->username;
$from_id = $update->message->from->id;
$name = $update->message->from->first_name;
}elseif($update->callback_query){
$data = $update->callback_query->data;
$chat_id = $update->callback_query->message->chat->id;
$title = $update->callback_query->message->chat->title;
$message_id = $update->callback_query->message->message_id;
$name = $update->callback_query->message->chat->first_name;
$user = $update->callback_query->message->chat->username;
$from_id = $update->callback_query->from->id;
}

	if($update->channel_post){
	$message = $update->channel_post;
	$message_id = $message->message_id;
$chat_id = $message->chat->id;
$text = $message->text;
$user = $message->chat->username;
$title = $message->chat->title;
$name = $message->author_signature;
$from_id = $message->chat->id;
	}
	if($update->edited_channel_post){
	$message = $update->edited_channel_post;
	$message_id = $message->message_id;
$chat_id = $message->chat->id;
$text = $message->text;
$user = $message->chat->username;
$name = $message->author_signature;
$from_id = $message->chat->id;
	}
	if($update->inline_query){
		$inline = $update->inline_query;
		$message = $inline;
		$user = $message->from->username;
$name = $message->from->first_name;
$from_id = $message->from->id;
$query = $message->query;
$text = $query;
		}
	if($update->chosen_inline_result){
		$message = $update->chosen_inline_result;
		$user = $message->from->username;
$name = $message->from->first_name;
$from_id = $message->from->id;
$inline_message_id = $message->inline_message_id;
$message_id = $inline_message_id;
$text = $message->query;
$query = $text;
		}
		$tc = $update->message->chat->type;
		$re = $update->message->reply_to_message;
		$re_id = $update->message->reply_to_message->from->id;
$re_user = $update->message->reply_to_message->from->username;
$re_name = $update->message->reply_to_message->from->first_name;
$re_messagid = $update->message->reply_to_message->message_id;
$re_chatid = $update->message->reply_to_message->chat->id;
$photo = $message->photo;
$video = $message->video;
$sticker = $message->sticker;
$file = $message->document;
$audio = $message->audio;
$voice = $message->voice;
$caption = $message->caption;
$photo_id = $message->photo[0]->file_id;
$video_id= $message->video->file_id;
$sticker_id = $message->sticker->file_id;
$file_id = $message->document->file_id;
$music_id = $message->audio->file_id;
$voice_id = $message->voice->file_id;
$forward = $message->forward_from_chat;
$forward_id = $message->forward_from_chat->id;
$title = $message->chat->title;
if($re){
	$forward_type = $re->forward_from->type;
$forward_name = $re->forward_from->first_name;
$forward_user = $re->forward_from->username;
	}else{
$forward_type = $message->forward_from->type;
$forward_name = $message->forward_from->first_name;
$forward_user = $message->forward_from->username;
$forward_id = $message->forward_from->id;
if($forward_name == null){
	$forward = $message->forward_from_chat;
$forward_id = $message->forward_from_chat->id;
$forward_title = $message->forward_from_chat->title;
	}
}
$title = $message->chat->title;

$sttings = json_decode(file_get_contents("media.json"),1);
$adminn = json_decode(file_get_contents("admin.json"),1);
$chat = json_decode(file_get_contents("chat.json"),1);
#######
$admin = 296369326; 
$userbot = (bot('getme',[])->result->username);
$tc = $update->message->chat->type;
$vvvzvvF = file_get_contents("vvvzvv.txt");
$vvvzvvF0 = file_get_contents("vvvzvv0.txt");
$vvvzvvF1= file_get_contents("vvvzvv1.txt");
$vvvzvvF5 = file_get_contents("vvvzvv2.txt");
$vvvzvvF6 = file_get_contents("vvvzvv3.txt");
$vvvzvvF20 = json_decode(file_get_contents('php://input'));
$vvvzvvF18 = $update->message;
$vvvzvvF13 = $vvvzvvF18->chat->id;
$vvvzvvF17 = $vvvzvvF18->text;
$meme = $vvvzvvF20->callback_query->data;
$vvvzvvF12 = $vvvzvvF20->callback_query->message->chat->id;
$vvvzvvF14 =  $vvvzvvF20->callback_query->message->message_id;
$vvvzvvF15 = $vvvzvvF18->from->first_name;
$vvvzvvF16 = $vvvzvvF18->from->username;
$vvvzvvF11 = $vvvzvvF18->from->id;
$vvvzvvF2 = explode("\n",file_get_contents("vvvzvv4.txt"));
$ArmoCH = explode("\n",file_get_contents("chall.txt"));
$vvvzvvGROP = explode("\n",file_get_contents("vvvzvvGR.txt"));
$vvvzvvF3 = count($vvvzvvF2)-1;
$vvvzvvGROPnt = count($vvvzvvGROP)-1;
$text_ch = $update->channel_post->text;
$ch_id = $update->channel_post->chat->id;
$getchall = file_get_contents("chall.txt");
$allgetch = explode("\n",$getchall);
$bot = file_get_contents("com.txt");
$cchcc = explode("\n",file_get_contents("chall.txt"));
$alllch = count($cchcc)-1;
$vvvzvvF11 = $vvvzvvF18->from->id;
$tc = $update->message->chat->type;
if($text_ch !== "/start" and !in_array($ch_id,$allgetch)){
file_put_contents("chall.txt","\n$ch_id",FILE_APPEND);
}
if($tc == 'private'){
if($message and !in_array($vvvzvvF11, $vvvzvvF2)) {
file_put_contents("vvvzvv4.txt", $vvvzvvF11."\n",FILE_APPEND);
}}
if($tc == 'group' or $tc == 'supergroup'){
if($message and !in_array($chat_id, $vvvzvvGROP)) {
file_put_contents("vvvzvvGR.txt", $chat_id."\n",FILE_APPEND);
}}
$vvvzvvF9 = file_get_contents("https://api.telegram.org/bot".API_KEY."/getChatMember?chat_id=$vvvzvvF0&user_id=".$vvvzvvF11);
$vvvzvvF10 = file_get_contents("https://api.telegram.org/bot".API_KEY."/getChatMember?chat_id=$vvvzvvF1&user_id=".$vvvzvvF11);
if($vvvzvvF18 && (strpos($vvvzvvF9,'"status":"left"') or strpos($vvvzvvF9,'"Bad Request: USER_ID_INVALID"') or strpos($vvvzvvF9,'"status":"kicked"') or strpos($vvvzvvF10,'"status":"left"') or strpos($vvvzvvF10,'"Bad Request: USER_ID_INVALID"') or strpos($vvvzvvF10,'"status":"kicked"'))!== false){
if($tc == 'private'){
bot('sendMessage', [
'chat_id'=>$chat_id,
'text'=>'*
âï¸Ø¹ÙÙÙ Ø§ÙØ§Ø´ØªØ±Ø§Ù ÙÙ ÙÙØ§Ø© Ø§ÙØ¨ÙØª Ø§ÙÙØ§Ù !*
','parse_mode'=>'markdown','reply_to_message_id'=>$message->message_id,
'reply_markup'=>json_encode([
'inline_keyboard'=>[
[['text'=>"- Ø§Ø¶ØºØ· ÙÙØ§ ÙÙØ§Ø´ØªØ±Ø§Ù . ",'url'=>"https://t.me/".str_replace("@","",$vvvzvvF0)]]
]
])
]);}}
$arr = ["/start","Ø§ÙØ³Ø­","ØªÙØ¹ÙÙ","Ø§","Øº","ØªØ¹Ø·ÙÙ"];
if(in_array($text,$arr)){
if($tc == 'group' or $tc == 'supergroup'){
if($vvvzvvF18 && (strpos($vvvzvvF9,'"status":"left"') or strpos($vvvzvvF9,'"Bad Request: USER_ID_INVALID"') or strpos($vvvzvvF9,'"status":"kicked"') or strpos($vvvzvvF10,'"status":"left"') or strpos($vvvzvvF10,'"Bad Request: USER_ID_INVALID"') or strpos($vvvzvvF10,'"status":"kicked"'))!== false){
bot('sendMessage', [
'chat_id'=>$chat_id,
'text'=>'*
âï¸Ø¹ÙÙÙ Ø§ÙØ§Ø´ØªØ±Ø§Ù ÙÙ ÙÙØ§Ø© Ø§ÙØ¨ÙØª Ø§ÙÙØ§Ù !*
','parse_mode'=>'markdown','reply_to_message_id'=>$message->message_id,
'reply_markup'=>json_encode([
'inline_keyboard'=>[
[['text'=>"- Ø§Ø¶ØºØ· ÙÙØ§ ÙÙØ§Ø´ØªØ±Ø§Ù . ",'url'=>"https://t.me/".str_replace("@","",$vvvzvvF0)]]
]
])
]);exit();
}}}
if($text == "/start" and $from_id == $admin and $tc == 'private'){
bot('sendmessage',[
"chat_id"=>$chat_id,
"text"=>"â¢ Ø§ÙÙØ§ Ø¨Ù ÙÙ ÙÙØ­Ø© Ø§ÙØ§ÙØ± Ø§ÙÙØ·ÙØ± Ø§ÙØ®Ø§ØµØ© Ø¨Ù", 'parse_mode'=>"MarkDown",
'disable_web_page_preview'=>'true',
'reply_markup'=>json_encode([ 
'inline_keyboard'=>[
[['text'=>'- Ø£ÙØ§ÙØ± Ø§ÙØ¥Ø´ØªØ±Ø§Ù Ø§ÙØ¥Ø¬Ø¨Ø§Ø±Ù Ø§ÙØ£ÙÙ  ' ,'callback_data'=>"vvvzvv"]],
[['text'=>'â¢ ÙØ¶Ø¹ ÙÙØ§Ø©  1ï¸â£' ,'callback_data'=>"vvvzvv0"],['text'=>'â¢ Ø­Ø°Ù ÙÙØ§Ø©  1ï¸â£' ,'callback_data'=>"delete11"]],
[['text'=>'â¢ ÙØ¶Ø¹ ÙÙØ§Ø© 2ï¸â£ ' ,'callback_data'=>"vvvzvv2"],['text'=>'â¢ Ø­Ø°Ù ÙÙØ§Ø©  2ï¸â£' ,'callback_data'=>"delete22"]],
[['text'=>'- Ø¹Ø±Ø¶ ÙÙÙØ§Øª Ø§ÙØ¥Ø´ØªØ±Ø§Ù  ' ,'callback_data'=>"vvvzvv4"]],
[['text'=>'- Ø£ÙØ§ÙØ± Ø§ÙØ¥Ø°Ø§Ø¹Ù ð' ,'callback_data'=>"vvvzvv"]],
[['text'=>'â¢ Ø§Ø±Ø³Ø§Ù Ø±Ø³Ø§ÙØ© ð' ,'callback_data'=>"."],['text'=>'â¢ Ø§Ø±Ø³Ø§Ù ØªÙØ¬ÙÙ ð' ,'callback_data'=>"."]],
[['text'=>'â¢ Ø®Ø§Øµ  ','callback_data'=>"vvvzvv5"],['text'=>'â¢ Ø®Ø§Øµ  ' ,'callback_data'=>"vvvzvv6"]],
[['text'=>'â¢ ÙÙÙØ§Øª ' ,'callback_data'=>"vvvzvvch"],['text'=>'â¢ ÙÙÙØ§Øª  ' ,'callback_data'=>"vvvzvvchtx"]],
[['text'=>'â¢ ÙØ¬ÙÙØ¹Ø§Øª ' ,'callback_data'=>"vvvzvvGro"],['text'=>'â¢ ÙØ¬ÙÙØ¹Ø§Øª ' ,'callback_data'=>"vvvzvvGr"]],
[['text'=>'- Ø¹Ø¯Ø¯ Ø§ÙÙÙÙØ§Øª  âï¸' ,'callback_data'=>"vvvzvv77"]],
[['text'=>'- Ø¹Ø¯Ø¯ Ø§ÙÙØ´ØªØ±ÙÙÙ  ' ,'callback_data'=>"vvvzvv7"],['text'=>'- Ø¹Ø¯Ø¯ Ø§ÙÙØ±ÙØ¨Ø§Øª','callback_data'=>"vvvzvv777"]],
[['text'=>'â¢ ØªÙØ¹ÙÙ Ø§ÙØªÙØ¨ÙÙ  - : ' ,'callback_data'=>"vvvzvv9"],['text'=>'â¢ ØªØ¹Ø·ÙÙ Ø§ÙØªÙØ¨ÙÙ â' ,'callback_data'=>"vvvzvv10"]],
[['text'=>'- ØªÙØ¬ÙÙ Ø±Ø³Ø§Ø¦Ù ÙÙ Ø§ÙØ£Ø¹Ø¶Ø§Ø¡','callback_data'=>"vvvzvv"]],
[['text'=>'â¢ ØªÙØ¹ÙÙ Ø§ÙØªÙØ¬ÙÙ  - : ' ,'callback_data'=>"vvvzvv11"],['text'=>'â¢ ØªØ¹Ø·ÙÙ Ø§ÙØªÙØ¬ÙÙ â' ,'callback_data'=>"vvvzvv12"]],
] 
])
]);
}
if($meme == "vvvzvv" ){
bot('EditMessageText',[
'chat_id'=>$vvvzvvF12,
'message_id'=>$vvvzvvF14,
"text"=>" â¢ Ø§ÙÙØ§ Ø¨Ù ÙÙ ÙÙØ­Ø© Ø§ÙØ§ÙØ± Ø§ÙÙØ·ÙØ± Ø§ÙØ®Ø§ØµØ© Ø¨Ù",
 'parse_mode'=>"MarkDown",
'disable_web_page_preview'=>'true',
'reply_markup'=>json_encode([ 
'inline_keyboard'=>[
[['text'=>'- Ø£ÙØ§ÙØ± Ø§ÙØ¥Ø´ØªØ±Ø§Ù Ø§ÙØ¥Ø¬Ø¨Ø§Ø±Ù Ø§ÙØ£ÙÙ  ' ,'callback_data'=>"vvvzvv"]],
[['text'=>'â¢ ÙØ¶Ø¹ ÙÙØ§Ø©  1ï¸â£' ,'callback_data'=>"vvvzvv0"],['text'=>'â¢ Ø­Ø°Ù ÙÙØ§Ø©  1ï¸â£' ,'callback_data'=>"delete11"]],
[['text'=>'â¢ ÙØ¶Ø¹ ÙÙØ§Ø© 2ï¸â£ ' ,'callback_data'=>"vvvzvv2"],['text'=>'â¢ Ø­Ø°Ù ÙÙØ§Ø©  2ï¸â£' ,'callback_data'=>"delete22"]],
[['text'=>'- Ø¹Ø±Ø¶ ÙÙÙØ§Øª Ø§ÙØ¥Ø´ØªØ±Ø§Ù  ' ,'callback_data'=>"vvvzvv4"]],
[['text'=>'- Ø£ÙØ§ÙØ± Ø§ÙØ¥Ø°Ø§Ø¹Ù ð' ,'callback_data'=>"vvvzvv"]],
[['text'=>'â¢ Ø§Ø±Ø³Ø§Ù Ø±Ø³Ø§ÙØ© ð' ,'callback_data'=>"."],['text'=>'â¢ Ø§Ø±Ø³Ø§Ù ØªÙØ¬ÙÙ ð' ,'callback_data'=>"."]],
[['text'=>'â¢ Ø®Ø§Øµ  ','callback_data'=>"vvvzvv5"],['text'=>'â¢ Ø®Ø§Øµ  ' ,'callback_data'=>"vvvzvv6"]],
[['text'=>'â¢ ÙÙÙØ§Øª ' ,'callback_data'=>"vvvzvvch"],['text'=>'â¢ ÙÙÙØ§Øª  ' ,'callback_data'=>"vvvzvvchtx"]],
[['text'=>'â¢ ÙØ¬ÙÙØ¹Ø§Øª ' ,'callback_data'=>"vvvzvvGro"],['text'=>'â¢ ÙØ¬ÙÙØ¹Ø§Øª ' ,'callback_data'=>"vvvzvvGr"]],
[['text'=>'- Ø¹Ø¯Ø¯ Ø§ÙÙÙÙØ§Øª  âï¸' ,'callback_data'=>"vvvzvv77"]],
[['text'=>'- Ø¹Ø¯Ø¯ Ø§ÙÙØ´ØªØ±ÙÙÙ  ' ,'callback_data'=>"vvvzvv7"],['text'=>'- Ø¹Ø¯Ø¯ Ø§ÙÙØ±ÙØ¨Ø§Øª','callback_data'=>"vvvzvv777"]],
[['text'=>'â¢ ØªÙØ¹ÙÙ Ø§ÙØªÙØ¨ÙÙ  - : ' ,'callback_data'=>"vvvzvv9"],['text'=>'â¢ ØªØ¹Ø·ÙÙ Ø§ÙØªÙØ¨ÙÙ â' ,'callback_data'=>"vvvzvv10"]],
[['text'=>'- ØªÙØ¬ÙÙ Ø±Ø³Ø§Ø¦Ù ÙÙ Ø§ÙØ£Ø¹Ø¶Ø§Ø¡','callback_data'=>"vvvzvv"]],
[['text'=>'â¢ ØªÙØ¹ÙÙ Ø§ÙØªÙØ¬ÙÙ  - : ' ,'callback_data'=>"vvvzvv11"],['text'=>'â¢ ØªØ¹Ø·ÙÙ Ø§ÙØªÙØ¬ÙÙ â' ,'callback_data'=>"vvvzvv12"]],
 ] 
   ])
]);
unlink("vvvzvv.txt");
}
if($meme == "vvvzvv0"){
bot('EditMessageText',[
    'chat_id'=>$vvvzvvF12,
    'message_id'=>$vvvzvvF14,
'text'=>'- Ø­Ø³ÙØ§Ù  Ø§ÙØ¢Ù ÙÙ Ø¨Ø¥Ø±Ø³Ø§Ù ÙØ¹Ø±Ù ÙÙØ§Ø©Ù ÙÙØªÙ ÙØ¶Ø¹Ù ÙÙ Ø®Ø¯ÙØ© Ø§ÙØ¥Ø´ØªØ±Ø§Ù Ø§ÙØ¥Ø¬Ø¨Ø§Ø±Ù ÙÙÙÙØ§Ø© Ø§ÙØ£ÙÙÙ  
#ÙØ«Ø§Ù :
âªï¸@shalsakin
',
 'reply_markup'=>json_encode([ 
      'inline_keyboard'=>[
[['text'=>'ð' ,'callback_data'=>"vvvzvv"]],
]])
]);
file_put_contents("vvvzvv.txt","vvvzvv0");
}
if($vvvzvvF17 and $vvvzvvF == "vvvzvv0" and $vvvzvvF11 == $admin){
bot("sendmessage",[
"chat_id"=>$vvvzvvF13,
"text"=>'- ÙÙØ¯ ØªÙ ÙØ¶Ø¹ Ø§ÙÙÙØ§Ø© Ø¨ÙØ¬Ø§Ø­  
- ÙÙ Ø¨Ø±ÙØ¹ Ø§ÙØ¨ÙØª Ø£Ø¯ÙÙ Ø¯Ø§Ø®Ù Ø§ÙÙÙØ§Ø©  ð',
 'reply_markup'=>json_encode([ 
      'inline_keyboard'=>[
[['text'=>'ð' ,'callback_data'=>"vvvzvv"]],
]])
]);
file_put_contents("vvvzvv0.txt","$vvvzvvF17");
unlink("vvvzvv.txt");
}
if($meme == "delete11"){
bot('EditMessageText',[
    'chat_id'=>$vvvzvvF12,
    'message_id'=>$vvvzvvF14,
'text'=>'- Ø­Ø³ÙØ§Ù ÙÙ Ø£ÙØª ÙØªØ£ÙØ¯ ÙÙ Ø£ÙÙ ØªØ±ÙØ¯ Ø­Ø°Ù Ø§ÙÙÙØ§Ø© ÙÙ Ø§ÙØ¥Ø´ØªØ±Ø§Ù Ø§ÙØ¥Ø¬Ø¨Ø§Ø±Ù  ð«
',
'reply_markup'=>json_encode([
'inline_keyboard'=>[[
['text'=>'â¢ ÙØ§  ', 'callback_data'=>'vvvzvv'],
['text'=>'â¢ ÙØ¹Ù  ','callback_data'=>'vvvzvv1'],
]    
]])
]);    
}
if($meme == "vvvzvv1"){
bot('EditMessageText',[
'chat_id'=>$vvvzvvF12,
'message_id'=>$vvvzvvF14,
'text'=>'- ÙÙØ¯ ØªÙ Ø­Ø°Ù Ø§ÙÙÙØ§Ø© Ø§ÙØ§ÙÙÙ ÙÙ Ø§ÙØ¥Ø´ØªØ±Ø§Ù Ø§ÙØ¥Ø¬Ø¨Ø§Ø±Ù Ø¨ÙØ¬Ø§Ø­  ',
'reply_markup'=>json_encode([ 
'inline_keyboard'=>[
ï¸[['text'=>'ð' ,'callback_data'=>"vvvzvv"]],
]])
]);
unlink("vvvzvv.txt");
unlink("vvvzvv0.txt");
}
if($meme == "vvvzvv2"){
bot('EditMessageText',[
'chat_id'=>$vvvzvvF12,
'message_id'=>$vvvzvvF14,
'text'=>'- Ø­Ø³ÙØ§Ù  Ø§ÙØ¢Ù ÙÙ Ø¨Ø¥Ø±Ø³Ø§Ù ÙØ¹Ø±Ù ÙÙØ§Ø©Ù ÙÙØªÙ ÙØ¶Ø¹Ù ÙÙ Ø®Ø¯ÙØ© Ø§ÙØ¥Ø´ØªØ±Ø§Ù Ø§ÙØ¥Ø¬Ø¨Ø§Ø±Ù ÙÙÙÙØ§Ø© Ø§ÙØ«Ø§ÙÙØ©  
#ÙØ«Ø§Ù :
âªï¸@shalsakin',
'reply_markup'=>json_encode([ 
'inline_keyboard'=>[
[['text'=>'ð' ,'callback_data'=>"vvvzvv"]],
]])
]);
file_put_contents("vvvzvv.txt","vvvzvv1");
}
if($vvvzvvF17 and $vvvzvvF == "vvvzvv1" and $vvvzvvF11 == $admin){
bot("sendmessage",[
"chat_id"=>$vvvzvvF13,
"text"=>'- ÙÙØ¯ ØªÙ ÙØ¶Ø¹ Ø§ÙÙÙØ§Ø© Ø¨ÙØ¬Ø§Ø­  
- ÙÙ Ø¨Ø±ÙØ¹ Ø§ÙØ¨ÙØª Ø£Ø¯ÙÙ Ø¯Ø§Ø®Ù Ø§ÙÙÙØ§Ø©  ð',
'reply_markup'=>json_encode([ 
'inline_keyboard'=>[
[['text'=>'ð' ,'callback_data'=>"vvvzvv"]],
]])
]);
file_put_contents("vvvzvv1.txt","$vvvzvvF17");
unlink("vvvzvv.txt");
}
if($meme == "delete22"){
bot('EditMessageText',[
'chat_id'=>$vvvzvvF12,
'message_id'=>$vvvzvvF14,
'text'=>'- Ø­Ø³ÙØ§Ù ÙÙ Ø£ÙØª ÙØªØ£ÙØ¯ ÙÙ Ø£ÙÙ ØªØ±ÙØ¯ Ø­Ø°Ù Ø§ÙÙÙØ§Ø© ÙÙ Ø§ÙØ¥Ø´ØªØ±Ø§Ù Ø§ÙØ¥Ø¬Ø¨Ø§Ø±Ù  ð«',
'reply_markup'=>json_encode([
'inline_keyboard'=>[
[
['text'=>'â¢ ÙØ§  ', 'callback_data'=>'vvvzvv'],
['text'=>'â¢ ÙØ¹Ù  ','callback_data'=>'vvvzvv3'],
]    
]])
]);    
}
if($meme == "vvvzvv3"){
bot('EditMessageText',[
'chat_id'=>$vvvzvvF12,
'message_id'=>$vvvzvvF14,
'text'=>'- ÙÙØ¯ ØªÙ Ø­Ø°Ù Ø§ÙÙÙØ§Ø© Ø§ÙØ«Ø§ÙÙØ© ÙÙ Ø§ÙØ¥Ø´ØªØ±Ø§Ù Ø§ÙØ¥Ø¬Ø¨Ø§Ø±Ù Ø¨ÙØ¬Ø§Ø­  ',
'reply_markup'=>json_encode([ 
'inline_keyboard'=>[
[['text'=>'ð' ,'callback_data'=>"vvvzvv"]],
]])
]);
unlink("vvvzvv.txt");
unlink("vvvzvv1.txt");
}
if($meme == "vvvzvv4"){
bot('EditMessageText',[
'chat_id'=>$vvvzvvF12,
'message_id'=>$vvvzvvF14,
'text'=>"- ÙØ°Ù ÙØ§Ø¦ÙØ© Ø§ÙÙÙÙØ§Øª Ø§ÙØ£Ø´ØªØ±Ø§Ù Ø§ÙØ§Ø¬Ø¨Ø§Ø±Ù  
- Ø§ÙÙÙØ§Ø© Ø§ÙØ§ÙÙÙ   $vvvzvvF0  
- Ø§ÙÙÙØ§Ø© Ø§ÙØ«Ø§ÙÙØ©   $vvvzvvF1 
ï¹ï¹ï¹ï¹ï¹ï¹ï¹ï¹ï¹ï¹ï¹ï¹",
'reply_markup'=>json_encode([ 
'inline_keyboard'=>[
[['text'=>'ð' ,'callback_data'=>"vvvzvv"]],
]])
]);
unlink("vvvzvv.txt");
}
if($meme == "vvvzvv5"){
bot('EditMessageText',[
'chat_id'=>$vvvzvvF12,
'message_id'=>$vvvzvvF14,
'text'=>"~ Ø£Ø±Ø³Ù Ø±Ø³Ø§ÙØªÙ ÙØ³ÙØªÙ ØªÙØ¬ÙÙÙØ§ ÙÙ [ $vvvzvvF3 ] ÙØ´ØªØ±Ù  ð ",
'reply_markup'=>json_encode([ 
'inline_keyboard'=>[
[['text'=>'ð' ,'callback_data'=>"vvvzvv"]],
]])
]);
file_put_contents("vvvzvv.txt","vvvzvv2");
}
if($vvvzvvF18 and $vvvzvvF == "vvvzvv2" and $vvvzvvF11 == $admin){
bot("sendmessage",[
"chat_id"=>$vvvzvvF13,
"text"=>'- ØªÙ Ø§ÙØªÙØ¬ÙÙ Ø¨ÙØ¬Ø§Ø­ ',
'reply_markup'=>json_encode([ 
'inline_keyboard'=>[
[['text'=>'ð' ,'callback_data'=>"vvvzvv"]],
]])
]);
for($i=0;$i<count($vvvzvvF2); $i++){
bot('forwardMessage', [
'chat_id'=>$vvvzvvF2[$i],
'from_chat_id'=>$vvvzvvF11,
'message_id'=>$vvvzvvF18->message_id
]);
unlink("vvvzvv.txt");
}
}
if($meme == "vvvzvv6"){
bot('EditMessageText',[
    'chat_id'=>$vvvzvvF12,
    'message_id'=>$vvvzvvF14,
'text'=>"~ Ø£Ø±Ø³Ù Ø±Ø³Ø§ÙØªÙ ÙØ³ÙØªÙ Ø¥Ø±Ø³Ø§ÙÙØ§ ÙÙ [ $vvvzvvF3 ] ÙØ´ØªØ±Ù  ð ",
 'reply_markup'=>json_encode([ 
      'inline_keyboard'=>[
[['text'=>'ð' ,'callback_data'=>"vvvzvv"]],
]])
]);
file_put_contents("vvvzvv.txt","vvvzvv3");
}
if($vvvzvvF17 and $vvvzvvF == "vvvzvv3" and $vvvzvvF11 == $admin){
bot("sendmessage",[
"chat_id"=>$vvvzvvF13,
"text"=>'- ØªÙ Ø§ÙÙØ´Ø± Ø¨ÙØ¬Ø§Ø­ ',
 'reply_markup'=>json_encode([ 
      'inline_keyboard'=>[
[['text'=>'ð' ,'callback_data'=>"vvvzvv"]],
]])
]);
for($i=0;$i<count($vvvzvvF2); $i++){
bot('sendMessage', [
'chat_id'=>$vvvzvvF2[$i],
'text'=>$vvvzvvF17
]);
unlink("vvvzvv.txt");
}
}
if($meme == "vvvzvvGro"){
bot('EditMessageText',[
'chat_id'=>$vvvzvvF12,
'message_id'=>$vvvzvvF14,
'text'=>"~ Ø£Ø±Ø³Ù Ø±Ø³Ø§ÙØªÙ ÙØ³ÙØªÙ ØªÙØ¬ÙÙÙØ§ ÙÙ [ $vvvzvvGROPnt ] ÙØ±ÙØ¨  ð ",
'reply_markup'=>json_encode([ 
'inline_keyboard'=>[
[['text'=>'ð' ,'callback_data'=>"vvvzvv"]],
]])
]);
file_put_contents("vvvzvv.txt","vvvzvvGro");
}
if($message and $vvvzvvF == "vvvzvvGro" and $vvvzvvF11 == $admin){
bot("sendmessage",[
"chat_id"=>$vvvzvvF13,
"text"=>'- ØªÙ Ø§ÙØªÙØ¬ÙÙ Ø¨ÙØ¬Ø§Ø­ ',
'reply_markup'=>json_encode([ 
'inline_keyboard'=>[
[['text'=>'ð' ,'callback_data'=>"vvvzvv"]],
]])
]);
for($i=0;$i<count($vvvzvvGROP);$i++){
bot('forwardMessage',[
'chat_id'=>$vvvzvvGROP[$i],
'from_chat_id'=>$vvvzvvF11,
'message_id'=>$message->message_id
]);
unlink("vvvzvv.txt");
}
}
if($meme == "vvvzvvGr"){
bot('EditMessageText',[
'chat_id'=>$vvvzvvF12,
'message_id'=>$vvvzvvF14,
'text'=>"~ Ø£Ø±Ø³Ù Ø±Ø³Ø§ÙØªÙ ÙØ³ÙØªÙ Ø¥Ø±Ø³Ø§ÙÙØ§ ÙÙ [ $vvvzvvGROPnt ] ÙØ±ÙØ¨  ð ",
'reply_markup'=>json_encode([ 
'inline_keyboard'=>[
[['text'=>'ð' ,'callback_data'=>"vvvzvv"]],
]])
]);
file_put_contents("vvvzvv.txt","vvvzvvGr");
}
if($vvvzvvF17 and $vvvzvvF == "vvvzvvGr" and $vvvzvvF11 == $admin){
bot("sendmessage",[
"chat_id"=>$vvvzvvF13,
"text"=>'- ØªÙ Ø§ÙÙØ´Ø± Ø¨ÙØ¬Ø§Ø­ ',
'reply_markup'=>json_encode([ 
'inline_keyboard'=>[
[['text'=>'ð' ,'callback_data'=>"vvvzvv"]],
]])
]);
for($i=0;$i<count($vvvzvvGROP);$i++){
bot('sendMessage',[
'chat_id'=>$vvvzvvGROP[$i],
'text'=>$vvvzvvF17
]);
unlink("vvvzvv.txt");
}
}
if($meme == "vvvzvvch"){
bot('EditMessageText',[
'chat_id'=>$vvvzvvF12,
'message_id'=>$vvvzvvF14,
'text'=>"~ Ø£Ø±Ø³Ù Ø±Ø³Ø§ÙØªÙ ÙØ³ÙØªÙ ØªÙØ¬ÙÙÙØ§ ÙÙ [ $alllch ] ÙÙØ§Ø©  ð ",
'reply_markup'=>json_encode([ 
'inline_keyboard'=>[
[['text'=>'ð' ,'callback_data'=>"vvvzvv"]],
]])
]);
file_put_contents("vvvzvv.txt","vvvzvvch");
}
if($message and $vvvzvvF == "vvvzvvch" and $vvvzvvF11 == $admin){
bot("sendmessage",[
"chat_id"=>$vvvzvvF13,
"text"=>'- ØªÙ Ø§ÙØªÙØ¬ÙÙ Ø¨ÙØ¬Ø§Ø­ ',
'reply_markup'=>json_encode([ 
'inline_keyboard'=>[
[['text'=>'ð' ,'callback_data'=>"vvvzvv"]],
]])
]);
for($i=0;$i<count($ArmoCH);$i++){
bot('forwardMessage',[
'chat_id'=>$ArmoCH[$i],
'from_chat_id'=>$vvvzvvF11,
'message_id'=>$message->message_id
]);
unlink("vvvzvv.txt");
}
}
if($meme == "vvvzvvchtx"){
bot('EditMessageText',[
'chat_id'=>$vvvzvvF12,
'message_id'=>$vvvzvvF14,
'text'=>"~ Ø£Ø±Ø³Ù Ø±Ø³Ø§ÙØªÙ ÙØ³ÙØªÙ Ø¥Ø±Ø³Ø§ÙÙØ§ ÙÙ [ $alllch ] ÙÙØ§Ø©  ð ",
'reply_markup'=>json_encode([ 
'inline_keyboard'=>[
[['text'=>'ð' ,'callback_data'=>"vvvzvv"]],
]])
]);
file_put_contents("vvvzvv.txt","vvvzvvoch");
}
if($vvvzvvF17 and $vvvzvvF == "vvvzvvoch" and $vvvzvvF11 == $admin){
bot("sendmessage",[
"chat_id"=>$vvvzvvF13,
"text"=>'- ØªÙ Ø§ÙÙØ´Ø± Ø¨ÙØ¬Ø§Ø­ ',
'reply_markup'=>json_encode([ 
'inline_keyboard'=>[
[['text'=>'ð' ,'callback_data'=>"vvvzvv"]],
]])
]);
for($i=0;$i<count($ArmoCH);$i++){
bot('sendMessage',[
'chat_id'=>$ArmoCH[$i],
'text'=>$vvvzvvF17
]);
unlink("vvvzvv.txt");
}
}
if($meme == "vvvzvv7"){
bot('EditMessageText',[
    'chat_id'=>$vvvzvvF12,
    'message_id'=>$vvvzvvF14,
'text'=>"- Ø¹Ø¯Ø¯ ÙØ´ØªØ±ÙÙÙ Ø§ÙØ¨ÙØª  [ $vvvzvvF3 ] ÙØ´ØªØ±Ù  ",
 'reply_markup'=>json_encode([ 
      'inline_keyboard'=>[
[['text'=>'ð' ,'callback_data'=>"vvvzvv"]],
]])
]);
unlink("vvvzvv.txt");
}
if($meme == "vvvzvv77"){
bot('EditMessageText',[
    'chat_id'=>$vvvzvvF12,
    'message_id'=>$vvvzvvF14,
'text'=>"- Ø¹Ø¯Ø¯ ÙÙÙØ§Øª Ø§ÙØ¨ÙØª  [ $alllch ] ÙÙØ§Ø©  ",
 'reply_markup'=>json_encode([ 
      'inline_keyboard'=>[
[['text'=>'ð' ,'callback_data'=>"vvvzvv"]],
]])
]);
unlink("vvvzvv.txt");
}
if($meme == "vvvzvv777"){
bot('EditMessageText',[
    'chat_id'=>$vvvzvvF12,
    'message_id'=>$vvvzvvF14,
'text'=>"- Ø¹Ø¯Ø¯ ÙØ±ÙØ¨Ø§Øª Ø§ÙØ¨ÙØª  [ $vvvzvvGROPnt ] ÙØ±ÙØ¨  ",
 'reply_markup'=>json_encode([ 
      'inline_keyboard'=>[
[['text'=>'ð' ,'callback_data'=>"vvvzvv"]],
]])
]);
unlink("vvvzvv.txt");
}
if($meme == "vvvzvv9"){
bot('EditMessageText',[
    'chat_id'=>$vvvzvvF12,
    'message_id'=>$vvvzvvF14,
'text'=>'- ØªÙ ØªÙØ¹ÙÙ Ø¯Ø®ÙÙ Ø§ÙÙØ´ØªØ±ÙÙÙ  ð',
 'reply_markup'=>json_encode([ 
      'inline_keyboard'=>[
[['text'=>'ð' ,'callback_data'=>"vvvzvv"]],
]])
]);
file_put_contents("vvvzvv2.txt","vvvzvv");
}
if($vvvzvvF17 == "/start" and $vvvzvvF5 == "vvvzvv" and $vvvzvvF11 != $admin){
bot("sendmessage",[
"chat_id"=>$admin,
"text"=>"- Ø¹Ø¶Ù Ø¬Ø¯ÙØ¯ ÙØ§Ù Ø¨Ø§ÙØ¯Ø®ÙÙ Ø§ÙÙ Ø§ÙØ¨ÙØª  
- Ø§ÙØ§Ø³Ù  [$vvvzvvF15](tg://user?id=$chat_id)  
- Ø§ÙÙØ¹Ø±Ù  [@$vvvzvvF16](tg://user?id=$chat_id)  
- Ø§ÙØ§ÙØ¯Ù  [$vvvzvvF11](tg://user?id=$chat_id)   
ï¹ï¹ï¹ï¹ï¹ï¹ï¹ï¹ï¹ï¹ï¹ï¹
~  Ø¹Ø¯Ø¯ Ø§ÙÙØ´ØªØ±ÙÙÙ  { $vvvzvvF3 }   ",
 'parse_mode'=>"MarkDown",
'disable_web_page_preview'=>'true',
]);
}
if($meme == "vvvzvv10"){
bot('EditMessageText',[
    'chat_id'=>$vvvzvvF12,
    'message_id'=>$vvvzvvF14,
'text'=>'- ØªÙ ØªØ¹Ø·ÙÙ Ø¯Ø®ÙÙ Ø§ÙÙØ´ØªØ±ÙÙÙ   ',
 'reply_markup'=>json_encode([ 
      'inline_keyboard'=>[
[['text'=>'ð' ,'callback_data'=>"vvvzvv"]],
]])
]);
unlink("vvvzvv.txt");
unlink("vvvzvv2.txt");
}
if($meme == "vvvzvv11"){
bot('EditMessageText',[
    'chat_id'=>$vvvzvvF12,
    'message_id'=>$vvvzvvF14,
'text'=>'- ØªÙ ØªÙØ¹ÙÙ ØªÙØ¬ÙÙ Ø§ÙØ±Ø³Ø§Ø¦Ù  ',
 'reply_markup'=>json_encode([ 
      'inline_keyboard'=>[
[['text'=>'ð' ,'callback_data'=>"vvvzvv"]],
]])
]);
file_put_contents("vvvzvv3.txt","vvvzvv");
}
if($vvvzvvF18 and $vvvzvvF6 == "vvvzvv" and $vvvzvvF11 != $admin){
bot('forwardMessage', [
'chat_id'=>$admin,
'from_chat_id'=>$vvvzvvF11,
'message_id'=>$vvvzvvF18->message_id
]);
}
if($vvvzvvF18 and $vvvzvvF6 == "vvvzvv" and $vvvzvvF11 == $admin ){
bot('sendMessage',[
'chat_id'=>$vvvzvvF18->reply_to_message->forward_from->id,
    'text'=>$vvvzvvF17,
    ]);
}
if($meme == "vvvzvv12"){
bot('EditMessageText',[
    'chat_id'=>$vvvzvvF12,
    'message_id'=>$vvvzvvF14,
'text'=>'- ØªÙ ØªØ¹Ø·ÙÙ ØªÙØ¬ÙÙ Ø§ÙØ±Ø³Ø§Ø¦Ù  ',
 'reply_markup'=>json_encode([ 
      'inline_keyboard'=>[
[['text'=>'ð' ,'callback_data'=>"vvvzvv"]],
]])
]);
unlink("vvvzvv.txt");
unlink("vvvzvv3.txt");
} 
$url = $update->message->entities[0]->type;
$linkurl = json_decode(file_get_contents("link.json"),1);
$name = $update->message->from->first_name;
if($url and !preg_match('#(.*)@(.*)#',$text) and !preg_match('#(.*)start(.*)#',$text)){
if($linkurl["murl"][$from_id] == null or $linkurl["murl"][$from_id] <= 2){
bot('sendmessage',[
'chat_id'=>$chat_id,
'text'=>"â¢*Ø¹Ø²ÙØ²Ù : *[$name](tg://user?id=$from_id) 
 ÙÙÙØ¹ Ø§Ø±Ø³Ø§Ù Ø§ÙØ±ÙØ§Ø¨Ø· ÙÙØ§ Ø³Ø£ÙÙÙ Ø¨Ø­Ø¶Ø±Ù Ø§Ø°Ø§ ÙØ±Ø±Øª Ø§ÙØ§Ø±Ø³Ø§Ù",
'reply_to_message_id'=>$update->message->message_id ,
'parse_mode'=>'markdown','disable_web_page_preview'=>true
]);
bot('deleteMessage',[
'chat_id'=>$chat_id,
'message_id'=>$update->message->message_id 
]);
}else{
bot('sendmessage',[
'chat_id'=>$chat_id,
'text'=>"â¢ *Ø¹Ø²ÙØ²Ù : *[$name](tg://user?id=$from_id) 
ØªÙ Ø­Ø¸Ø±Ù ÙÙ Ø§ÙÙØ¬ÙÙØ¹Ø© ",'reply_to_message_id'=>$update->message->message_id ,
'parse_mode'=>'markdown','disable_web_page_preview'=>true 
]);
bot('banChatMember',[
'chat_id'=>$chat_id,
'user_id'=>$from_id 
]);
bot('deleteMessage',[
'chat_id'=>$chat_id,
'message_id'=>$update->message->message_id 
]);
}
$linkurl["murl"][$from_id]+=1;
file_put_contents("link.json",json_encode($linkurl));
}

$re_id = $update->message->reply_to_message->from->id;
$re_na = $update->message->reply_to_message->from->id;
$rt = $update->message->reply_to_message;
$ad = json_decode(file_get_contents("ad.json"),1);
function sadmin($arr){
file_put_contents("ad.json",json_encode($arr));
}
if($rt and $text == 'Ø±ÙØ¹ Ø§Ø¯ÙÙ'){
if($from_id == $admin){
bot('sendmessage',[
'chat_id'=>$chat_id,
'text'=>"â¢ Ø§ÙØ¹Ø¶Ù - [$re_na](tg://user?id=$re_id)  
â¢ ØªÙ Ø±ÙØ¹Ù Ø§Ø¯ÙÙ
 ",
]);
$ad[$re_id]="ok";
sadmin($ad);
}}
if($rt and $text == 'ØªÙØ²ÙÙ Ø§Ø¯ÙÙ'){
if($from_id == $admin){
bot('sendmessage',[
'chat_id'=>$chat_id,
'text'=>"â¢ Ø§ÙØ¹Ø¶Ù - [$re_na](tg://user?id=$re_id)  
â¢ ØªÙ ØªÙØ²ÙÙÙ 
 ",
]);
unset($ad[$re_id]);
sadmin($ad);
}}
if($rt and $text == "Ø­Ø¸Ø±"){
if($ad[$from_id] == "ok" or in_array($from_id, $admin)){
bot('unbanChatMember',[
'chat_id'=>$chat_id,
'user_id'=>$re_id
]);
}
}
if($text == "/start"){
bot('sendmessage',[
'chat_id'=>$chat_id,
'text'=>"â¢ Ø§ÙÙØ§ Ø¨Ù Ø¹Ø²ÙØ²Ù
- Ø§ÙØ§ Ø§ÙÙÙ Ø¨ØªØ£ÙÙÙ ÙÙØ§ÙØ´Ø© ÙÙØ§Ø© Ø®Ø§ØµØ© ÙÙ Ø§Ø±Ø³Ø§Ù Ø§ÙØ±ÙØ§Ø¨Ø·",
]);
}


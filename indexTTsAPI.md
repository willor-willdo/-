## API documentationhttp://127.0.0.1:7866/API Recorder14 API endpoints 



Choose one of the following ways to interact with the API.

1. Install the python client ([docs](https://www.gradio.app/guides/getting-started-with-the-python-client)) if you don't already have it installed.

```
copy
$ pip install gradio_client
```

2. Find the API endpoint below corresponding to your desired function in the app. Copy the code snippet, replacing the placeholder values with your own input data. Or use the API Recorder to automatically generate your API requests.

### api_name: /on_preset_select

```
copyfrom gradio_client import Client

client = Client("http://127.0.0.1:7866/")
result = client.predict(
		selected_display_name="请选择预设样音",
		api_name="/on_preset_select"
)
print(result)
```

#### Accepts 1 parameter:

------

selected_display_name Literal['请选择预设样音', '0000', '女-不二-拟真女声（精品）', '女-乐彤-电商带货', '女-可可-甜美少女', '女-学姐-知识分享', '女-小玉-电商带货（精品）', '女-小艾-儿童绘本', '女-小芳-温馨解说', '女-御姐-性感御姐', '女-微瑕-甄嬛配音（精品）', '女-晓晨-推文配音', '女-曼波-游戏解说（精品）', '女-月晨-细腻柔情', '女-格美-轻松叙事', '女-梦梦-柔情女声', '女-欣瑶-知心姐姐', '女-灵萱-清甜女声', '女-点妹-抖音热门（精品）', '女-玉玉-娱乐专用', '女-甜心-呆萌甜美', '女-绒绒-广告专用', '女-菜菜-科普女声', '女-萝莉-甜美萝莉', '女-超幼-儿童配音', '女-逗嫂-拟真女声', '女-通用-通用百搭', '男-之秋-电影解说', '男-云希-推文配音', '男-云邪-恐怖悬疑（精品）', '男-味仙-视频解说', '男-咕噜-游戏解说（精品）', '男-四郎-甄嬛配音', '男-夜凯-惊悚悬疑', '男-奇闻-恐怖悬疑（精品）', '男-奈斯-电影解说（精品）', '男-姥爷-悬疑解说', '男-子涵-深沉男声', '男-宇轩-低沉舒缓', '男-小新-特色配音', '男-小田-知识分享', '男-小陈-电影解说（精品）', '男-御史-历史解说（精品）', '男-披风-深沉情感（精品）', '男-无花-风趣解说', '男-樊登-知识付费', '男-比特-电台男声（精品）', '男-浩泽-动物世界', '男-海明-情感男声', '男-渣辉-特色配音', '男-激石-节奏男声', '男-熊二-特色配音', '男-猴哥-特色配音', '男-老二-悬疑解说（精品）', '男-豆包-知识分享', '男-阿生-电影解说', '男-青丘-赛事解说', '男-鸿轩-温柔情感（精品）'] Default: "请选择预设样音"

The input value that is provided in the "选择预设样音" Dropdown component.

#### Returns tuple of 2 elements

------

[0] filepath

The output value that appears in the "🎵 参考音频" Audio component.

------

[1] str

The output value that appears in the "📊 状态信息" Html component.

### api_name: /on_upload_audio

```
copyfrom gradio_client import Client, handle_file

client = Client("http://127.0.0.1:7866/")
result = client.predict(
		uploaded_file=handle_file('https://github.com/gradio-app/gradio/raw/main/test/test_files/sample_file.pdf'),
		api_name="/on_upload_audio"
)
print(result)
```

#### Accepts 1 parameter:

------

uploaded_file filepath **Required**

The input value that is provided in the "📁 上传样音" Uploadbutton component.

#### Returns tuple of 3 elements

------

[0] Literal['请选择预设样音', '0000', '女-不二-拟真女声（精品）', '女-乐彤-电商带货', '女-可可-甜美少女', '女-学姐-知识分享', '女-小玉-电商带货（精品）', '女-小艾-儿童绘本', '女-小芳-温馨解说', '女-御姐-性感御姐', '女-微瑕-甄嬛配音（精品）', '女-晓晨-推文配音', '女-曼波-游戏解说（精品）', '女-月晨-细腻柔情', '女-格美-轻松叙事', '女-梦梦-柔情女声', '女-欣瑶-知心姐姐', '女-灵萱-清甜女声', '女-点妹-抖音热门（精品）', '女-玉玉-娱乐专用', '女-甜心-呆萌甜美', '女-绒绒-广告专用', '女-菜菜-科普女声', '女-萝莉-甜美萝莉', '女-超幼-儿童配音', '女-逗嫂-拟真女声', '女-通用-通用百搭', '男-之秋-电影解说', '男-云希-推文配音', '男-云邪-恐怖悬疑（精品）', '男-味仙-视频解说', '男-咕噜-游戏解说（精品）', '男-四郎-甄嬛配音', '男-夜凯-惊悚悬疑', '男-奇闻-恐怖悬疑（精品）', '男-奈斯-电影解说（精品）', '男-姥爷-悬疑解说', '男-子涵-深沉男声', '男-宇轩-低沉舒缓', '男-小新-特色配音', '男-小田-知识分享', '男-小陈-电影解说（精品）', '男-御史-历史解说（精品）', '男-披风-深沉情感（精品）', '男-无花-风趣解说', '男-樊登-知识付费', '男-比特-电台男声（精品）', '男-浩泽-动物世界', '男-海明-情感男声', '男-渣辉-特色配音', '男-激石-节奏男声', '男-熊二-特色配音', '男-猴哥-特色配音', '男-老二-悬疑解说（精品）', '男-豆包-知识分享', '男-阿生-电影解说', '男-青丘-赛事解说', '男-鸿轩-温柔情感（精品）']

The output value that appears in the "选择预设样音" Dropdown component.

------

[1] str

The output value that appears in the "📊 状态信息" Html component.

------

[2] filepath

The output value that appears in the "🎵 参考音频" Audio component.

### api_name: /on_delete_audio_click

```
copyfrom gradio_client import Client

client = Client("http://127.0.0.1:7866/")
result = client.predict(
		selected_audio="请选择预设样音",
		api_name="/on_delete_audio_click"
)
print(result)
```

#### Accepts 1 parameter:

------

selected_audio Literal['请选择预设样音', '0000', '女-不二-拟真女声（精品）', '女-乐彤-电商带货', '女-可可-甜美少女', '女-学姐-知识分享', '女-小玉-电商带货（精品）', '女-小艾-儿童绘本', '女-小芳-温馨解说', '女-御姐-性感御姐', '女-微瑕-甄嬛配音（精品）', '女-晓晨-推文配音', '女-曼波-游戏解说（精品）', '女-月晨-细腻柔情', '女-格美-轻松叙事', '女-梦梦-柔情女声', '女-欣瑶-知心姐姐', '女-灵萱-清甜女声', '女-点妹-抖音热门（精品）', '女-玉玉-娱乐专用', '女-甜心-呆萌甜美', '女-绒绒-广告专用', '女-菜菜-科普女声', '女-萝莉-甜美萝莉', '女-超幼-儿童配音', '女-逗嫂-拟真女声', '女-通用-通用百搭', '男-之秋-电影解说', '男-云希-推文配音', '男-云邪-恐怖悬疑（精品）', '男-味仙-视频解说', '男-咕噜-游戏解说（精品）', '男-四郎-甄嬛配音', '男-夜凯-惊悚悬疑', '男-奇闻-恐怖悬疑（精品）', '男-奈斯-电影解说（精品）', '男-姥爷-悬疑解说', '男-子涵-深沉男声', '男-宇轩-低沉舒缓', '男-小新-特色配音', '男-小田-知识分享', '男-小陈-电影解说（精品）', '男-御史-历史解说（精品）', '男-披风-深沉情感（精品）', '男-无花-风趣解说', '男-樊登-知识付费', '男-比特-电台男声（精品）', '男-浩泽-动物世界', '男-海明-情感男声', '男-渣辉-特色配音', '男-激石-节奏男声', '男-熊二-特色配音', '男-猴哥-特色配音', '男-老二-悬疑解说（精品）', '男-豆包-知识分享', '男-阿生-电影解说', '男-青丘-赛事解说', '男-鸿轩-温柔情感（精品）'] Default: "请选择预设样音"

The input value that is provided in the "选择预设样音" Dropdown component.

#### Returns tuple of 2 elements

------

[0] str

The output value that appears in the "📊 状态信息" Html component.

------

[1] str

The output value that appears in the "value_12" Html component.

### api_name: /on_confirm_delete

```
copyfrom gradio_client import Client

client = Client("http://127.0.0.1:7866/")
result = client.predict(
		selected_audio="请选择预设样音",
		api_name="/on_confirm_delete"
)
print(result)
```

#### Accepts 1 parameter:

------

selected_audio Literal['请选择预设样音', '0000', '女-不二-拟真女声（精品）', '女-乐彤-电商带货', '女-可可-甜美少女', '女-学姐-知识分享', '女-小玉-电商带货（精品）', '女-小艾-儿童绘本', '女-小芳-温馨解说', '女-御姐-性感御姐', '女-微瑕-甄嬛配音（精品）', '女-晓晨-推文配音', '女-曼波-游戏解说（精品）', '女-月晨-细腻柔情', '女-格美-轻松叙事', '女-梦梦-柔情女声', '女-欣瑶-知心姐姐', '女-灵萱-清甜女声', '女-点妹-抖音热门（精品）', '女-玉玉-娱乐专用', '女-甜心-呆萌甜美', '女-绒绒-广告专用', '女-菜菜-科普女声', '女-萝莉-甜美萝莉', '女-超幼-儿童配音', '女-逗嫂-拟真女声', '女-通用-通用百搭', '男-之秋-电影解说', '男-云希-推文配音', '男-云邪-恐怖悬疑（精品）', '男-味仙-视频解说', '男-咕噜-游戏解说（精品）', '男-四郎-甄嬛配音', '男-夜凯-惊悚悬疑', '男-奇闻-恐怖悬疑（精品）', '男-奈斯-电影解说（精品）', '男-姥爷-悬疑解说', '男-子涵-深沉男声', '男-宇轩-低沉舒缓', '男-小新-特色配音', '男-小田-知识分享', '男-小陈-电影解说（精品）', '男-御史-历史解说（精品）', '男-披风-深沉情感（精品）', '男-无花-风趣解说', '男-樊登-知识付费', '男-比特-电台男声（精品）', '男-浩泽-动物世界', '男-海明-情感男声', '男-渣辉-特色配音', '男-激石-节奏男声', '男-熊二-特色配音', '男-猴哥-特色配音', '男-老二-悬疑解说（精品）', '男-豆包-知识分享', '男-阿生-电影解说', '男-青丘-赛事解说', '男-鸿轩-温柔情感（精品）'] Default: "请选择预设样音"

The input value that is provided in the "选择预设样音" Dropdown component.

#### Returns tuple of 3 elements

------

[0] Literal['请选择预设样音', '0000', '女-不二-拟真女声（精品）', '女-乐彤-电商带货', '女-可可-甜美少女', '女-学姐-知识分享', '女-小玉-电商带货（精品）', '女-小艾-儿童绘本', '女-小芳-温馨解说', '女-御姐-性感御姐', '女-微瑕-甄嬛配音（精品）', '女-晓晨-推文配音', '女-曼波-游戏解说（精品）', '女-月晨-细腻柔情', '女-格美-轻松叙事', '女-梦梦-柔情女声', '女-欣瑶-知心姐姐', '女-灵萱-清甜女声', '女-点妹-抖音热门（精品）', '女-玉玉-娱乐专用', '女-甜心-呆萌甜美', '女-绒绒-广告专用', '女-菜菜-科普女声', '女-萝莉-甜美萝莉', '女-超幼-儿童配音', '女-逗嫂-拟真女声', '女-通用-通用百搭', '男-之秋-电影解说', '男-云希-推文配音', '男-云邪-恐怖悬疑（精品）', '男-味仙-视频解说', '男-咕噜-游戏解说（精品）', '男-四郎-甄嬛配音', '男-夜凯-惊悚悬疑', '男-奇闻-恐怖悬疑（精品）', '男-奈斯-电影解说（精品）', '男-姥爷-悬疑解说', '男-子涵-深沉男声', '男-宇轩-低沉舒缓', '男-小新-特色配音', '男-小田-知识分享', '男-小陈-电影解说（精品）', '男-御史-历史解说（精品）', '男-披风-深沉情感（精品）', '男-无花-风趣解说', '男-樊登-知识付费', '男-比特-电台男声（精品）', '男-浩泽-动物世界', '男-海明-情感男声', '男-渣辉-特色配音', '男-激石-节奏男声', '男-熊二-特色配音', '男-猴哥-特色配音', '男-老二-悬疑解说（精品）', '男-豆包-知识分享', '男-阿生-电影解说', '男-青丘-赛事解说', '男-鸿轩-温柔情感（精品）']

The output value that appears in the "选择预设样音" Dropdown component.

------

[1] str

The output value that appears in the "📊 状态信息" Html component.

------

[2] filepath

The output value that appears in the "🎵 参考音频" Audio component.

### api_name: /on_cancel_delete

```
copyfrom gradio_client import Client

client = Client("http://127.0.0.1:7866/")
result = client.predict(
		api_name="/on_cancel_delete"
)
print(result)
```

#### Accepts 0 parameters:

#### Returns 1 element

------

str

The output value that appears in the "📊 状态信息" Html component.

### api_name: /on_upload_subtitle

```
copyfrom gradio_client import Client, handle_file

client = Client("http://127.0.0.1:7866/")
result = client.predict(
		uploaded_file=handle_file('https://github.com/gradio-app/gradio/raw/main/test/test_files/sample_file.pdf'),
		api_name="/on_upload_subtitle"
)
print(result)
```

#### Accepts 1 parameter:

------

uploaded_file filepath **Required**

The input value that is provided in the "📄 上传字幕" Uploadbutton component.

#### Returns tuple of 2 elements

------

[0] str

The output value that appears in the "📝 文本" Textbox component.

------

[1] str

The output value that appears in the "📊 状态信息" Html component.

### api_name: /on_generate_subtitle

```
copyfrom gradio_client import Client, handle_file

client = Client("http://127.0.0.1:7866/")
result = client.predict(
		audio_file=handle_file('https://github.com/gradio-app/gradio/raw/main/test/test_files/audio_sample.wav'),
		text_content="Hello!!",
		api_name="/on_generate_subtitle"
)
print(result)
```

#### Accepts 2 parameters:

------

audio_file filepath **Required**

The input value that is provided in the "🎵 生成结果" Audio component. The FileData class is a subclass of the GradioModel class that represents a file object within a Gradio interface. It is used to store file data and metadata when a file is uploaded. Attributes: path: The server file path where the file is stored. url: The normalized server URL pointing to the file. size: The size of the file in bytes. orig_name: The original filename before upload. mime_type: The MIME type of the file. is_stream: Indicates whether the file is a stream. meta: Additional metadata used internally (should not be changed).

------

text_content str **Required**

The input value that is provided in the "📝 文本" Textbox component.

#### Returns 1 element

------

str

The output value that appears in the "📊 状态信息" Html component.

### api_name: /on_clear_cache_click

```
copyfrom gradio_client import Client

client = Client("http://127.0.0.1:7866/")
result = client.predict(
		api_name="/on_clear_cache_click"
)
print(result)
```

#### Accepts 0 parameters:

#### Returns tuple of 2 elements

------

[0] str

The output value that appears in the "📊 状态信息" Html component.

------

[1] str

The output value that appears in the "value_30" Html component.

### api_name: /on_confirm_clear_cache

```
copyfrom gradio_client import Client

client = Client("http://127.0.0.1:7866/")
result = client.predict(
		api_name="/on_confirm_clear_cache"
)
print(result)
```

#### Accepts 0 parameters:

#### Returns 1 element

------

str

The output value that appears in the "📊 状态信息" Html component.

### api_name: /on_cancel_clear_cache

```
copyfrom gradio_client import Client

client = Client("http://127.0.0.1:7866/")
result = client.predict(
		api_name="/on_cancel_clear_cache"
)
print(result)
```

#### Accepts 0 parameters:

#### Returns 1 element

------

str

The output value that appears in the "📊 状态信息" Html component.

### api_name: /on_input_text_change

```
copyfrom gradio_client import Client

client = Client("http://127.0.0.1:7866/")
result = client.predict(
		text="Hello!!",
		max_tokens_per_sentence=120,
		api_name="/on_input_text_change"
)
print(result)
```

#### Accepts 2 parameters:

------

text str **Required**

The input value that is provided in the "📝 文本" Textbox component.

------

max_tokens_per_sentence float Default: 120

The input value that is provided in the "分句最大Token数" Slider component.

#### Returns 1 element

------

dict(headers: list[Any], data: list[list[Any]], metadata: dict(str, list[Any] | None) | None)

The output value that appears in the "value_61" Dataframe component.

### api_name: /on_input_text_change_1

```
copyfrom gradio_client import Client

client = Client("http://127.0.0.1:7866/")
result = client.predict(
		text="Hello!!",
		max_tokens_per_sentence=120,
		api_name="/on_input_text_change_1"
)
print(result)
```

#### Accepts 2 parameters:

------

text str **Required**

The input value that is provided in the "📝 文本" Textbox component.

------

max_tokens_per_sentence float Default: 120

The input value that is provided in the "分句最大Token数" Slider component.

#### Returns 1 element

------

dict(headers: list[Any], data: list[list[Any]], metadata: dict(str, list[Any] | None) | None)

The output value that appears in the "value_61" Dataframe component.

### api_name: /update_prompt_audio

```
copyfrom gradio_client import Client

client = Client("http://127.0.0.1:7866/")
result = client.predict(
		api_name="/update_prompt_audio"
)
print(result)
```

#### Accepts 0 parameters:

#### Returns 1 element

### api_name: /gen_single_with_status

```
copyfrom gradio_client import Client, handle_file

client = Client("http://127.0.0.1:7866/")
result = client.predict(
		prompt=handle_file('https://github.com/gradio-app/gradio/raw/main/test/test_files/audio_sample.wav'),
		text="Hello!!",
		infer_mode="普通推理",
		max_text_tokens_per_sentence=120,
		sentences_bucket_max_size=4,
		param_5=True,
		param_6=0.8,
		param_7=30,
		param_8=1,
		param_9=0,
		param_10=3,
		param_11=10,
		param_12=600,
		api_name="/gen_single_with_status"
)
print(result)
```

#### Accepts 13 parameters:

------

prompt filepath **Required**

The input value that is provided in the "🎵 参考音频" Audio component. The FileData class is a subclass of the GradioModel class that represents a file object within a Gradio interface. It is used to store file data and metadata when a file is uploaded. Attributes: path: The server file path where the file is stored. url: The normalized server URL pointing to the file. size: The size of the file in bytes. orig_name: The original filename before upload. mime_type: The MIME type of the file. is_stream: Indicates whether the file is a stream. meta: Additional metadata used internally (should not be changed).

------

text str **Required**

The input value that is provided in the "📝 文本" Textbox component.

------

infer_mode Literal['普通推理', '批次推理'] Default: "普通推理"

The input value that is provided in the "⚙️ 推理模式" Radio component.

------

max_text_tokens_per_sentence float Default: 120

The input value that is provided in the "分句最大Token数" Slider component.

------

sentences_bucket_max_size float Default: 4

The input value that is provided in the "分句分桶的最大容量（批次推理生效）" Slider component.

------

param_5 bool Default: True

The input value that is provided in the "do_sample" Checkbox component.

------

param_6 float Default: 0.8

The input value that is provided in the "top_p" Slider component.

------

param_7 float Default: 30

The input value that is provided in the "top_k" Slider component.

------

param_8 float Default: 1

The input value that is provided in the "temperature" Slider component.

------

param_9 float Default: 0

The input value that is provided in the "length_penalty" Number component.

------

param_10 float Default: 3

The input value that is provided in the "num_beams" Slider component.

------

param_11 float Default: 10

The input value that is provided in the "repetition_penalty" Number component.

------

param_12 float Default: 600

The input value that is provided in the "max_mel_tokens" Slider component.

#### Returns tuple of 2 elements

------

[0] filepath

The output value that appears in the "🎵 生成结果" Audio component.

------

[1] str

The output value that appears in the "📊 状态信息" Html component.
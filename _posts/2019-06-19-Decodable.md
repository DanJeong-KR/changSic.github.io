---
layout: post
title:  " [iOS : Codable]중첩된 JSON 데이터를 원하는 부분만 Codable 을 활용해서 가져오기! "
subtitle:
categories: iOS
tags: note
---
<img width="5749" alt="중첩된 JSON 데이터를 원하는 부분만 Codable 을 활용해서 가져오기" src="https://user-images.githubusercontent.com/38423205/59762029-2fd7c200-92d1-11e9-8aeb-9a48b98eda24.png">

### [마인드맵 보기](https://github.com/changSic/Task/files/3305838/convertJsonObjectToCodable.pdf)

JSON 데이터를 Decodable 프로토콜을 채택한 struct 로 만들어서 파싱하는 과정을 아주 세세하게 해부했습니다!

* JSONObject 파싱하기
* JSONArray 파싱하기
* Codable 을 이용했을 때
* CodingKey 와 decoder 의 container 를 어떻게 써야 할 것인가

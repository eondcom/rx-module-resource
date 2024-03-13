# Version History
- v.1.7.1(2024-03-13)
  - PHP8 대응
- v.1.7.0(2013-03-20)

# Bug List
- Error #0 "Attempt to assign property "item_srl" on null" in modules/resource/resource.controller.php on line 276
  객체를 먼저 선언하지 않고 속성을 추가하려 하고 있습니다. 오래된 자료에서 종종 사용하던 코딩 방식이나 최근 PHP에서는 허용되지 않으니, 에러 메시지에 포함된 파일명과 줄 번호를 참고하여 수정하세요.
  modules/resource/resource.controller.php:276

글 본문에 이미지 파일 업로드 했을 때 발생함.
> $dargs 추가
> new Object -> new BaseObject 로 변경.
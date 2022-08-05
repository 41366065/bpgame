# API�ĵ�
### Ŀǰ���е�api���붼���� global/Assests/bplus_api.js ��
---
## ��Ƶ����
ʹ��ȫ�ֱ���**bplayer(Bvideo��)**����Ƶ���в���  
```
bplayer.jump_at(t)	  // ��ת����t��

bplayer.now_time();	// ������Ƶ�������ڵ�����(double)

bplayer.total_time();  // ������Ƶ����ʱ��(double)

bplayer.pause(); 	  // ��Ƶ��ͣ

bplayer.is_pause();    // �����Ƿ���ͣ(bool)

bplayer.fullscreen();  // ��Ƶȫ��

bplayer.is_fullscreen(); // �����Ƿ�ȫ��

Bvideo.time2second("2:30") // static������ ����2:30��������150.0��
```
---
## ��ͼ����
### ����htmlԪ��
**appendToContainer** ��ʾʹ��api������Ԫ���Ƿ�����idΪ"game-container"��div��  
��div����������Ƶ֮�ϣ��������Ϊ����Ƶ�Ϸ�����˸�һ������Ƕ����Ϸ  
**attributes** ��������htmlԪ�ص�����  
**style** ��������htmlԪ�ص�css style
```
// ����html img
create_img(src, appendToContainter=false, zIndex=1, attributes=null, style=null)

// ����html button
create_button(onclick=null, appendToContainter=true, zIndex=1, attributes=null, style=null)

// ���ط�װ��html canvas��BWindow��
create_window(rx, ry, rwidth=-1, rheight=-1, appendToContainter=true, zIndex=0)
/* (rx, ry, rwidth, right) ��ʾ��Ը�Ԫ�صĶ�λ�Ϳ��
    ��(0.5, 0.5, 0.4, 0.2) ��ʾ�ڸ�Ԫ�ؾ��е�λ�ã���Ϊ��Ԫ�ص�0.4�� ��Ϊ0.2
    Ĭ��rwidth��rheightΪ-1 ��ʾ��������(0.5, 0.5, -1, -1) === (0.5, 0.5, 1, 1) 
    ��̬��ͼ�뾡������BWindow�Ͻ���  */
```
	
### ��ͼ
ʹ�� **BWindow** �� **canvas** �ϻ�ͼ

```
var window = create_window(0.5, 0.5);	// ����һ��������Ļ�� ȫ���Ļ���

window.setStyle(pixelated);	// ����canvas ���ʵ���ʽ��pixelatedΪ���õ�����style

var img = create_img(src, false); 	// ����һ��img��false��ʾ���ӵ�container��

window.draw_img(img, 0.5, 0.5, 0.2, 0.2); // �ڻ����ϻ�һ�����еģ���߾�Ϊ����20%��img

window.draw_rectangle(0.5, 0.5, 0.2, 0.2, "rgba(255, 0, 0, 1.0)"); // �ڻ����ϻ�һ�����еģ���߾�Ϊ����20%�ĺ�ɫ����

window.draw_font("bpgame", 0.5, 0.5, hollow=false); // �ڻ���������д�֣� hollow��ʾ�����Ƿ��ο�

window.clear();	// ��������������ݣ�һ������֡����
```
ע�⣺draw_img()�����imgδ�������ʱ���첽�ȴ�img�������ٻ�ͼ  
��ϸ�����ɲμ�api�ļ��е� **BWindow** ��

---
## ����������֡����
Ŀǰ���������м��ʼ������������ܳ���������������...
```
start_key_listener(); // ���ô˺����Կ�����������
getkeydown(keycode['k']); // ��ǰ֡�Ƿ���k��
getkeyhold(keycode['k']); // ��ǰ֡�Ƿ�סk��
bupdate(handler);	// ��һ��handler�����󶨣�ÿһ֡���е���
```

---
## �ļ�IO
�ļ�IO��δ��������ԣ��뾡��ֻ��������ʾ����load�������ر�����Դ
```
let req = {location: "local", data: "seyana/img/note/red.png"};
var url = load(req); // �����᷵���ļ�����չurl
var img = create_img(url);

//����ֱ��
var img = load(req, (url) => create_img(url));

// load(url, handler)�� ��handler��Ϊfalseʱ����ʹ��handler�����ص����ݲ�����handler��ֵ

```

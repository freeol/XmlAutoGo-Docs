`>>Tags <./tags.html>`_

Webdriver tags
========================
Webdriver tags is the webdriver's controller.

<D_ADD_COOKIE/>
#######################
summary
 Add cookies.
eg.
::
 <d_add_cookie>
  my='abc';
  myinfo='add by XmlAutoGo.exe';
 </d_add_cookie>
notes
 none

<D_CLICKABLE/>
#######################
summary
 Click the loaded element(The selector is support ['ID', 'NAME', 'CLASS_NAME', 'XPATH', 'LINK_TEXT', 'PARTIAL_LINK_TEXT', 'TAG_NAME', 'CSS_SELECTOR']).
eg.
::
 <d_clickable timeout="10">ID=myid</d_clickable>
notes
 "timeout" is the times is waitting for load.(default is seconds). 

<D_DOWNLOAD/>
#######################
summary
 Download the file to the local path from the url's address .
eg.
::
 <d_download id="imgs{!index}" path="{!img_path}">{!link_url}</d_download>
notes
 | "id" is the key of the local file. if don't set "id", the id will be the file's name.
 | "path" is the local path.
 | The tag's content("{!link_url}") is the download from address.

<D_INPUT/>
#######################
summary
 Input the text into the text element.
eg.
::
 <d_input select="id=kw" timeout="10">xmlautogo test input test</d_input>
notes
 | "select" is support ['ID', 'NAME', 'CLASS_NAME', 'XPATH', 'LINK_TEXT', 'PARTIAL_LINK_TEXT', 'TAG_NAME', 'CSS_SELECTOR']
 | "timeout" is the times is waitting for load.(default is seconds). 

<D_JAVASCRIPT/>
#######################
summary
 Add javascript into the browser.
eg.
::
 <d_javascript>
    alert('hello word!');
 </d_javascript>
notes
 | In the tag also support public method.
 | 1. ADDJS_SETVAR(key, value)
 |  Set into the variable.

<D_REFRESH/>
#######################
summary
 Refresh the page.
eg.
::
 <d_refresh/>
notes
 none

<D_SCREENSHOT/>
#######################
summary
 Screenshot the browser.
eg.
::
 <d_screenshot>D:/screenshots/test.png</d_screenshot>
notes
 The tag's content is the image's saved path.

<D_SLEEP/>
#######################
summary
 The process's sleep's times(default seconds).
eg.
::
 <d_sleep>1</d_sleep>
notes
 none

<D_SWITCH_WIN/>
#######################
summary
 Switch the browser' window.
eg.
::
 <d_switch_win>1</d_switch_win>
notes
 The tag's content is the number of the browser' windows(Left to Right).

<D_TEXT_AS_VAR/>
#######################
summary
 Set the element text as a variable.
eg.
::
 <d_text_as_var id="passcode">xpath=/html/body/div/div[2]/p[3]/b</d_text_as_var>
notes
 | "id" is the variable's name.
 | The tag's content is the element's selector.

<D_QUIT/>
#######################
summary
 Quit the webdriver.
eg.
::
 <quit/>
notes
 none

<D_UPLOAD/>
#######################
summary
 Auto upload files by browser.
eg.1(one file).
::
 <d_upload by="Open" path="D:/test">"test.txt"</d_upload>

eg.2(more than one files).
::
 <d_upload by="Open" path="D:/test">["test.txt", "test1.txt"]</d_upload>

notes
 | "by" is the browser's upload window's name
 |     (English is "Open", Chinese is "打开", Japanese is "開く" and so on).
 | "path" is the upload file's local path.
 | The tag's content is the local path's files name.

<D_URL/>
#######################
summary
 Browser access address.
eg.
::
 <d_url>http://www.baidu.com</d_url>
notes
 none

<D_WAIT_FOR/>
#######################
summary
 Wait for the element has been loaded(The selector is support ['ID', 'NAME', 'CLASS_NAME', 'XPATH', 'LINK_TEXT', 'PARTIAL_LINK_TEXT', 'TAG_NAME', 'CSS_SELECTOR']).
eg.
::
 <d_wait_for timeout="10">ID=myid</d_wait_for>
notes
 "timeout" is the times is waitting for load.(default is seconds). 


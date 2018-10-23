`>>Tags <./tags.html>`_

Lang tags
==========================
Lang tags is the xml scripts' controller.

<ADD/>
#######################
summary
 Add item into the end of a list or array variable.
eg.
::
 <add id="t2">"add is ok"</add>
notes
 "id" is the variable's name


<BREAK/>
#######################
summary
 Breaks out of the innermost enclosing "<for/>".
eg.
::
 <for range="range(1,4)">
  <if>
    <when test="{!index}==2">
      <break/>
    </when>
  </if>
  <d_javascript>console.log('{!index}')</d_javascript>
 </for>
notes
 none

<CALL/>
#######################
summary
 Call the method or module's method
eg.
::
 <call name="test_func" parameters="{'a':2, 'b':1}"></call>
 <call name="myModule.func1" parameters="{'a':2, 'b':1}"></call>
notes
 | "name" is the method's name, the method's parameters is a json type.
 | It also can use "modulename.methodname" to call module's method with the "name". 

<CALL_EXEC/>
#######################
summary
 Call the (*.exe) file to execute
eg.
::
 <call name="kill_by_port" cmd="8888"/>
 <call name="C:/test.exe" cmd="a b c"/>
notes
 | "name" is the (*.exe) file's name, if there is no '.exe' in the name, the script will call the (*.exe) file in the AutoXmlGo's folder("/bin" ).
 | "cmd" is the file's arguments.

<CONTINUE/>
#######################
summary
 Continues with the next iteration of the loop.
eg.
::
 <for range="range(1,4)">
  <if>
   <when test="{!index}==2"><continue/></when>
  </if>
  <d_javascript>console.log('{!index}')</d_javascript>
 </for>
notes
 none
 
<COROUTINES/>
#######################
summary
 Support concurrent execution by coroutines.
eg.
::
<coroutines>
	<coroutine_func name="test1" parameters="{'msg':'1'}"/>
	<coroutine_func name="test2" parameters="{'msg':'2'}"/>
	<coroutine_func name="test3" parameters="{'msg':'3'}"/>
	<coroutine_func name="tM.test4" parameters="{'msg':'4'}"/>
	<coroutine_func name="test1" parameters="{'msg':'5'}"/>
	<coroutine_func name="test2" parameters="{'msg':'6'}"/>
	<coroutine_func name="test3" parameters="{'msg':'7'}"/>
	<coroutine_func name="tM.test5" parameters="{'msg':'8'}"/>
</coroutines>
notes
 none

<COROUTINE_FUNC/>
#######################
summary
 Call the function in coroutines.
eg.
::
 <coroutine_func name="test1" parameters="{'msg':'1'}"/>
notes
 none

<COROUTINE_EXEC/>
#######################
summary
 Call the (*.exe) file to execute in coroutines.
eg.
::
 <call name="kill_by_port" cmd="8888"/>
notes
 none

<DEBUG/>
#######################
summary
 Write log into logs' file.
eg.
::
 <debug>test1:{!test1.a}</debug>
notes
 none

<DOWNLOAD/>
#######################
summary
 Download the file to the local path from the url's address .
eg.
::
 <download id="imgs{!index}" path="{!img_path}">{!link_url}</download>
notes
 | "id" is the key of the local file. if don't set "id", the id will be the file's name.
 | "path" is the local path.
 | The tag's content("{!link_url}") is the download from address.

<ELIF/>
#######################
summary
 The mean is else if clause would run.
eg.
 Reference if_tag_

notes
 none

<ELSE/>
#######################
summary
 The mean is else clause would run.
eg.
 Reference if_tag_

notes
 none

<EVAL/>
#######################
summary
 The string variable evaluated.
eg.
::
 <variable>test="{'a':1}";</variable>
 <eval id="test2">{!test}</eval>
notes
 | If the "id" is not setted, the variable "test" would be a json type.
 | If "id" is setted, the new variable "test2" would be a json type.

<F2V/>
#######################
summary
 Use file's path to be variable.
eg.
::
 <f2v type="image" key="file1" as_key="file_variable"/>
notes
 | "type" is the space where saved in memory.("image" is in the image memory.) 
 | "key" is the key in selected type memory.
 | "as_key" is to be variable name

<FOR/>
#######################
summary
 The for tag is used to iterate over the elements of a iterable object.
eg 1.
::
 <for range="(0, 5)">
  <d_javascript>console.log('{!index}');</d_javascript>
 </for>
notes
 | "range" is returns an iterator of integers suitable.
 | "{!index}" is the index of the range.
eg 2.
::
 <for items="{!test_list}" var="item">
  <d_javascript>console.log('{!item}', '{!index}');</d_javascript>
 </for>
notes
 | "items" is a iterable object.
 | "var" is the variable would be used in the loop.
 | "{!index}" is the index of the range.

<FUNC/>
#######################
summary
 Defined a function method.
eg.
::
 <func name="test_func" parameters="{'a':1, 'b':[0,1,2,3]}">
  <variable>
   func_var=1;
   func_var2="2";
  </variable>
  <d_javascript>console.log('{!a}, {!b}, {!func_var}, {!func_var2}');</d_javascript>
 </func>
notes
 | "name" is the function's name.
 | "parameters" is the function's initialization parameters.

.. _if_tag:

<IF/>
#######################
summary
 | The if implement traditional control flow constructs.
 | <when/> is the if conditions. 
 | <elif/> is the else if conditions. 
 | <else/> is the else other conditions. 
eg.
::
 <if>
  <when test="0">
   <d_javascript>console.log('if-when');</d_javascript>
  </when>
  <elif test="{!test_if}=='123'">
   <d_javascript>console.log('if-elif');</d_javascript>
  </elif>
  <else>
   <d_javascript>console.log('if-else');</d_javascript>
  </else>
 </if>
notes
 "test" is the conditions(type boolean).

<IMPORT/>
#######################
summary
 Import the other xml's scripts module files into the main scripts file.
eg.
::
 <import>ucar_58.xml</import>
notes
 | The file path is support absolute path and relative path.

<INSERT/>
#######################
summary
 Insert a item into a list.
eg.
::
 <insert id="t2" index="1">"insert is ok"</insert>
notes
 | "id" is the list's name.
 | "index" is insert index of the array.

<MODULE/>
#######################
summary
 Defined a module.
eg.
::
 <module name="myModule">

  <variable>
   m_v=1;
  </variable>

  <func name="test" parameters="{'a':0, 'b':0}">
   <variable>
    m_v2=2;
   </variable>
   <d_javascript>console.log('{!m_v}, {!m_v2}')</d_javascript>
   <for range="(0, 5)">
   <d_javascript>console.log('index:{!index}')</d_javascript>
   </for>
   <if>
    <when test="{!m_v}=={!a}">
     <d_javascript>console.log('test_func if-when');</d_javascript>
    </when>
    <elif test="{!m_v}=={!b}">
     <d_javascript>console.log('test_func ELIF');</d_javascript>
    </elif>
   </if>
  </func>
 </module>
notes
 none

<PUT/>
#######################
summary
 Add or Update the json type variable.
eg.
::
 <put id="t1" key="b">2</put>
notes
 | "id" is the name of json type variable.
 | "key" is the key in the json type variable.
 | The tag's content is the key's value.

<RETURN/>
#######################
summary
 The end of the function method.
eg.
::
 <func name="test" parameters="{'a':''}">
  <d_javascript>console.log('func start')</d_javascript>
  <if>
   <when test="{a}=='abc'">
    <return/>
   </when>
  </if>
  <d_javascript>console.log('func end')</d_javascript>
 </func>
 <call name="test" parameters="{'a':'abc'}"/>
notes
 none

<SCRIPT/>
#######################
summary
 The outermost layer of the scripts's file.
eg.
::
 <script name="myscript" info="some thing">
    ......
 </script>
notes
 none

<SET/>
#######################
summary
 New or update a variable.
eg.
::
 <set id="t3">"abc"</set>
notes
 | "id" is the variable's name.
 | The tag's content is the variable's new value.

<SLEEP/>
#######################
summary
 The process's sleep's times(default seconds).
eg.
::
 <SLEEP>1</SLEEP>
notes
 none

<VARIABLE/>
#######################
summary
 Defined variables.
eg.
::
 <variable>img_path='D:/screenshots/'</variable>
 <d_screenshots>{!img_path}test.png</d_screenshots>
 
notes
 Support array, json, string, integer, bool and float types.
 

<WHEN/>
#######################
summary
 The if tag's conditions' tag.
eg.
 Reference if_tag_
notes

<ZIP/>
#######################
summary
 Compress files into a zip files.
eg.
::
<variable>
	testdir='D:/workspace/XmlAutoGo/examples/test';
</variable>
<zip path="{!testdir}" filename="test1" compress_path="{!testdir}"/>
<zip path="{!testdir}" filename="test2">
[('{!testdir}', 'f1', 'nf1'), ('{!testdir}', 'f2', 'nf2'), ('{!testdir}', 'f3', 'nf3')]
</zip>
 
notes
 | "path" is the created file(*.zip)'s directory.
 | "filename" is the created file(*.zip)'s name.
 | There are two way to compress files like ↑example.
 |   1.If the "compress_path" is setted, the path's folder will be compressed.
 |   2.The tag's content to point what the files will be compressed.
 
 


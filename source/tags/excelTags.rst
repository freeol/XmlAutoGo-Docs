`Tags <./tags.html>`_
==========================

Excel tags
==========================

<XLS_EXCEL/>
#######################
summary
 Defined excel's file(.xls).
eg.
::
 <xls_excel name="test.xlsx" path="{!excel_path}">
  <xls_sheet index="0" title="test1">
   <xls_value cell="A1">test excel value</xls_value>
   <xls_img cell="A5" width="255" height="50">{!test1}</xls_img>
  </xls_sheet>
  <xls_sheet index="1">
   <xls_img cell="A1" width="255" height="50">{!test1}</xls_img>
   <xls_img cell="A55"  width="255" height="50">{!test2}</xls_img>
  </xls_sheet>
 </xls_excel>
notes
 | "name" is the excel's name.
 | "path" is the excel's path.

<XLS_IMG/>
#######################
summary
 Insert a img into the excel.
eg.
::
 <xls_img cell="A5" width="255" height="50">d:/test.png</xls_img>
notes
 | "cell" is the position of the sheet.
 | "width" is the width of the image.
 | "height" is the height of the image.
 | The tag's content is the image's local path.

<XLS_SHEET/>
#######################
summary
 Defined a sheet in the excel file.
eg.
::
 <xls_sheet index="0" title="test1">
  <xls_value cell="A1">test excel value</xls_value>
  <xls_img cell="A5" width="255" height="50">{!test1}</xls_img>
 </xls_sheet>
notes
 | "index" is the index of the excel's sheet.
 | "title" is the sheet's name.

<XLS_VALUE/>
#######################
summary
 Insert text into the excel.
eg.
::
 <xls_value cell="A1">test excel value</xls_value>
notes
 | "cell" is the position of the sheet.
 | The tag's content is the input text.

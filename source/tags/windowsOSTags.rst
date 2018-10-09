`>>Tags <./tags.html>`_

Windows OS tags
==========================

<W_CURSOR_CLICK_LEFT/>
#######################
summary
  Mouse left key click once.
eg.
::
 <w_cursor_click_left/>
notes
 none

<W_CURSOR_CLICK_RIGHT/>
#######################
summary
 Mouse right key click once.
eg.
::
 <w_cursor_click_right/>
notes
 none

<W_CURSOR_POS/>
#######################
summary
 Set the mouse position.
eg.
::
 <w_cursor_pos x="0" y="0"/>
notes
 none

<W_DIRS_CLEAR/>
#######################
summary
 Clear the directory's files
eg.
::
 <w_dirs_clear>{!file_path}</w_dirs_clear>
notes
 none

<W_DIRS_CLEAR_ALL/>
#######################
summary
 Clear the directory's files and directories.
eg.
::
 <w_dirs_clear_all>{!file_path}</w_dirs_clear_all>
notes
 Waring:It's a danger step.

<W_FILE_COPY/>
#######################
summary
 Copy from file to the new path.
eg.
::
 <w_file_copy from="{!from_file_path}" to="{!to_file_path}"/>
notes
 

<W_FILE_DEL/>
#######################
summary
 Delete the file or directory.
eg.
::
 <w_file_del>{!file_path}</w_file_del>
notes
  Waring:It's a danger step

<W_FILE_MOVE/>
#######################
summary
 Move the file from to.
eg.
::
 <w_file_move from="{!from_file_path}" to="{!to_file_path}"/>
notes
 none

<W_FILE_READ/>
#######################
summary
 Read file's text as a variable.
eg.
::
 <w_file_read id="vars">{!file_path}</w_file_read>
notes
 | "id" is the variable's name.
 | The tag's content is the read file's path.

<W_FILE_RENAME/>
#######################
summary
 Rename the file.
eg.
::
 <w_file_rename from="{!from_file_path}" to="{!to_file_path}"/>
notes
 none


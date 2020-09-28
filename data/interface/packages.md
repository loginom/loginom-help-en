# ![ ](..\images\icons\system_object_18\package_default.svg)Packages

The main operations with [Packages](../quick-start/package.md) are listed on this page.

This page can be opened in two ways:

* using the ![ ](..\images\icons\system_object_18\package_default.svg)*Packages* button in [Address bar](.\addres-bar.md);
* using the [Navigation](./main-menu.md#navigatsiya) panel, selecting the ![ ](..\images\icons\system_object_18\package_default.svg)*Packages* section.

## Interface

* ![ ](..\images\icons\toolbar-controls\new_default.svg) **Create** enables to open a window to set a path and name of the new *Package*, it also enables to open this empty *Package* after saving. The following buttons enable to perform the following operations ![ ](..\images\icons\toolbar-controls\down_default.svg):
   * ![ ](..\images\icons\toolbar-controls\temporary_default.svg) **New Draft** enables to create a temporary *Package* without current saving.
* ![ ](..\images\icons\toolbar-controls\open_default.svg) **Open** enables to open the selection window of the existing *Package*.
* ![ ](..\images\icons\toolbar-controls\save_default.svg) **Save** enables to save the selected *Package*. The following buttons enable to perform the following operations ![ ](..\images\icons\toolbar-controls\down_default.svg):
   * ![ ](..\images\icons\toolbar-controls\save-as_default.svg) **Save as** enables to save the selected *Package* under a new name, and/or using another available path.
* ![ ](..\images\icons\toolbar-controls\save-all_default.svg) **Save all** is similar to the *Save* button for all opened *Packages*.
* ![ ](..\images\icons\toolbar-controls\publish_default.svg) **Publish**[^1] enables to open a window for the *Package* publication.
* ![ ](..\images\icons\toolbar-controls\edit_default.svg) **Properties** enables to open the [properties](#svoystva-paketa) configuration window of the selected *Package*.
* ![ ](..\images\icons\toolbar-controls\close_default.svg) **Close** enables to close the selected *Package*.
* ![ ](..\images\icons\toolbar-controls\close-all_default.svg) **Close all** enables to close all opened *Packages*.

[^1]: It is available only for the editions with possibility to publish [Web Services](../integration/web-services/publishing-web-service.md).

When closing the *Package* with unsaved changes, you will be requested to save it with the following variants:

* **Yes** will save and close this *Package*.
* **No** will cancel changes (the *Package* will be closed without saving!).
* **Cancel** will stop closing of the *Package* or further closing of still not closed *Packages*.

Opened *Packages* are listed in the table:

* **Name** is a name of the *Package*. It complies with the file name without extension set to the proper identifier.
* **Path** is a path to the opened *Package*. The path is specified from the root directory in the server version. The absolute path is specified for the Desktop version. More detailed information is provided in the [file storage](../location_user_files.md).
* **Version** is a version of the opened *Package*. It is configured in its *Properties*.
* **Published** shows whether the *Package* was published.

It is possible to sort the list for these fields in ascending order ![ ](../images/icons/toolbar-controls/low-to-hight_default.svg), in descending order ![ ](../images/icons/toolbar-controls/hight-to-low_default.svg), or to cancel sorting.

The context menu called by the right mouse button click, for the most part, enables to repeat the set listed above:

* For the opened *Packages*:
   * ![ ](..\images\icons\toolbar-controls\save_default.svg) **Save package**
   * ![ ](..\images\icons\toolbar-controls\save-as_default.svg) **Save package as…**
   * ![ ](..\images\icons\toolbar-controls\edit_default.svg) **Edit properties…**
   * ![ ](..\images\icons\blank.svg) **Show in folder** enables to open the folder containing the selected *Package* and takes focus on it.
   * ![ ](..\images\icons\toolbar-controls\close_default.svg) **Close package…**
   * ![ ](..\images\icons\blank.svg) **Close other packages…** enables to close all *Packages*, with the exception of the selected one.
* For the free zone:
   * ![ ](..\images\icons\toolbar-controls\new_default.svg) **New package…**
   * ![ ](..\images\icons\toolbar-controls\temporary_default.svg) **New draft**
   * ![ ](..\images\icons\toolbar-controls\save-all_default.svg) **Save all packages**
   * ![ ](..\images\icons\toolbar-controls\close-all_default.svg) **Close all packages…**
* General:
   * ![ ](..\images\icons\toolbar-controls\refresh_default.svg) **Refresh** enables to refresh a list.

Hot keys are available for some commands:

* %kbd F2 % — edit properties;
* %kbd Ctrl O % — open the *Package*;
* %kbd Ctrl S % — save the *Package*;
* %kbd Ctrl Shift S % — save all *Packages*;
* %kbd Alt P % — publication.

## Package Properties

It enables to set the following parameters of the *Package*:

* **Name** — the *Package* name is specified. Editing is possible only for the *Draft*. It will be set to the file name and correct identifier after saving.
* **Version** enables to specify the *Package* version. Version `1.0.0` is used by default.
* ![ ](..\images\icons\checkbox-states\checked_default.svg) **Use relative paths of the base package** must be enabled in the *Package* with base node, if this node has relative paths to files, or it is assumed to use paths in base nodes relative to this *Package*. This option is disabled by default.

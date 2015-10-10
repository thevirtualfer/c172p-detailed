Exporting .ac files on FGFS


(1) First, you need install ac3d import/export into your blender/addons.
    Please, don't use the official ac3d import/export. Our version has some customization.

(2) You have two types of groups. Blender groups and ac3d groups. These are independent groups.
    When exporting, don't assume that blender groups will be exported as ac3d groups because they will not.

    To create an ac3d group, do the following :
    
    (a) Create an empty and name it as something.group. (ie, if you want a light ac3d group, create an empty and name it light.group)

    (b) Parent objects that will be grouped to this empty.

    * This doesn't impede you to have an object (ie, a cube) with a name ending with .group. The ac3d group will be generated only if the object is a empty.

(3) The script doesn't export anything if you are in Edit Mode. Please, switch to Object Mode before exporting.

(4) The objects exported are those in the views where you locked the scene's camera and view. If you unlock a view, and the layer is not locked in any other view, the
    objects on that layer will not be exported.

    * The lock/unlock button is in the right of the layers menu in the 3D view

(5) Textures moved to Textures folder. Before, the exporter did copy all texture files to the folder it generates the .ac file.
    Now it prepends "Texture/" on all texture entries of the .ac file.

(6) Working on to allow subfolders into "Textures/" folder. It doesn't work yet. All the script does is append "Texture/" before the name of the image file, ignoring the path.

(7) After the change, YOU MUST create your blend file into "Models/BlendFiles/" folder. So, it is better you start doing this from now, to avoid future problems.

(8) All the models are loaded by c172p.xml file. So, all are relative to "Models/" folder, doesn't matter where the .ac file effectively resides on the tree. All textures are relative to "Models/" folder, and will reside inside the "Models/Textures/" folder and subfolder. So, export your ac3d model to where you think is more logical it resides, but have in mind that it will be viewed as it resides in the "Models/" folder when the sim starts.

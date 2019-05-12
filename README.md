# School of Activism e-learning template 

This is an example of an e-learning package with part of the visual identity for The Activism School, a project by Greenpeace Spain and Novact. If you know html you can clone this repository, add your content and create a SCORM package that can be uploaded to Moodle or any other LMS that supports this format.

## Create your lesson

### 1 - Clone or download this lesson

```bash
git clone https://github.com/greenpeace/gpes-activism-school-elearning-template.git
```

**[Download](https://github.com/greenpeace/gpes-activism-school-elearning-template/archive/master.zip)**

### 2 - Edit this lesson 

You just need a code editor like [Brackets](http://brackets.io/). This lesson uses [Bootstrap](https://getbootstrap.com/) and [jQuery](https://jquery.com/) the world’s most popular libraries. Read their documentation for more information.

## Create an elearning SCORM package

### 1 - Link and configure

Once you have finished your lesson, uncomment this html line at the end of index.html:

```html
<script src="https://storage.googleapis.com/gp-misc/e-learning/scormfunctions.js"></script>
```

You should also customise this variables:

```html
<script>
    var pageScore = 1;
    var minCompletedTime = 30;
</script>
```

- The `pageScore` is added when the user leaves the page and should be between 0 and 100.
- The `minCompletedTime` is the minimum ammount of time (in seconds) for the presentation to be considered complete.

If you create more than one html files, you should do this step in all your html files.

### 2 - Edit the table of contents

You can have multiple html pages in the same SCROM package. This example has only one, `index.html` 

To add or remove them to the table of contents you need to modify [imsmanifest.xml](imsmanifest.xml) with a text editor like [Brackets](http://brackets.io/). **Look at the examples** in the sections `<organizations>` `<item>` and `<resources>` of this xml. And edit it carefully!

### 3 - Package and upload

Create the SCORM package (a zip file):

```bash
cd this-repository-folder
zip -r mylesson.zip *
```

Upload `mylesson.zip` to [Moodle, as a SCORM package](https://docs.moodle.org/36/en/SCORM_settings). (It should work with any **L**earning **M**anagement **S**ystem that supports SCORM).

### Notes

Please note that LMSes like Moodle have many options to configure their SCORM lessons. Please test your package and read your LMS documentation.

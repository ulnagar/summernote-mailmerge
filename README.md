# summernote-mailmerge
A plugin for the [Summernote](https://github.com/summernote/summernote/) WYSIWYG editor.

summernote-mailmerge will insert defined merge field names at the cursor position in the Editor.

### Installation

#### 1. Include JS

Include the following code after Summernote:

```html
<script src="summernote-mailmerge.js"></script>
```

#### 2. Supported languages

Currently available in English!

#### 3. Summernote options

````javascript
$('.summernote').summernote({
    toolbar:[
        ['style',['style']],
        ['font',['bold','italic','underline','clear']],
        ['fontname',['fontname']],
        ['color',['color']],
        ['para',['ul','ol','paragraph']],
        ['height',['height']],
        ['table',['table']],
        ['insert',['mailmerge','media','link','hr']], // 'mailmerge', is the dropdown menu
        ['view',['fullscreen','codeview']],
        ['help',['help']]
    ],
    mailmerge: {
        menu: [
            ['Parent Name', '::parent_name::'], // adds an option in the Mail Merge dropdown for "Parent Name" which inserts the text "::parent_name::"
            ['Report Type', '::report_type::'],
            ['Report Date', '::report_month::']
        ]
    }
});
````

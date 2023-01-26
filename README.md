# Purpose of Drag-n-drop builder
Convert any frontend app into an editable frontend app. Give the users of your frontend-app power to modify that frontend-app. Drag-n-drop builder provide a Builder web component. The resulting user interface is defined in a json format. The Builder web component takes a json and emits a json of the resulting user interface. The Schema of the json format is described in this [gist](https://github.com/dragndropbuilder/builder-examples/wiki/Json-Schema-for-data-exchange).

# Drag-n-drop Builder Examples

## Sample for Salesforce Cloud Applications
Developers can integrate VideoStation drag-n-drop UI builder in their javascript applications by including the script tag as shown below. 
```
<script src="https://unpkg.com/@videostation/reportbuilder@latest/elements.js"></script>
``` 

To instantiate the drag-n-drop builder in a javascript application, use web-component vs-form-builder. 
```
<body>
    <vs-form-builder></vs-form-builder>
</body>
```  
![image](https://user-images.githubusercontent.com/107889902/214405403-fef25596-2d3d-499a-83ea-0c09a8f12b1c.png)

| | Link |
-- | -- 
Angular| [https://stackblitz.com/edit/angular-ivy-7h82w5?file=src%2Fapp%2Fapp.component.ts](https://stackblitz.com/edit/angular-ivy-7h82w5?file=src%2Fapp%2Fapp.component.ts)
React | [https://stackblitz.com/edit/react-ts-n8s1ok?file=App.tsx](https://stackblitz.com/edit/react-ts-n8s1ok?file=App.tsx)
Vanilla JavaScript | [https://stackblitz.com/edit/js-wxtylw?file=index.js](https://stackblitz.com/edit/js-wxtylw?file=index.js)

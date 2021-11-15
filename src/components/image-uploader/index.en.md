# ImageUploader

<code src="./demos/demo1.tsx"></code>

# API

## ImageUploader

| Name          | Description                                                                                                                                                              | Type                                                      | Default   |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------- | --------- |
| value         | List of uploaded files                                                                                                                                                   | `FileItem[]`                                              | -         |
| defaultValue  | Default list of uploaded files                                                                                                                                           | `FileItem[]`                                              | -         |
| onChange      | Triggered when the list of uploaded files changing                                                                                                                       | `(files: FileItem[]) => void`                             | -         |
| accept        | The file types, `image/gif` `image/jpeg` `image/jpg` `image/png`                                                                                                         | `string`                                                  | `image/*` |
| multiple      | Whether to support selecting multiple pictures                                                                                                                           | `boolean`                                                 | `false`   |
| maxCount      | To control how many pictures to be uploaded at most, the upload button would be automatically hidden if the number is exceeded, `0` means no limit                       | `number`                                                  | `0`       |
| onCountExceed | Triggered when the number of pictures selected by the user exceeds the maximum limit                                                                                     | `(exceed: number) => void`                                | -         |
| disableUpload | Whether to disable the upload button                                                                                                                                     | `boolean`                                                 | `false`   |
| showUpload    | Whether to display the upload button                                                                                                                                     | `boolean`                                                 | `true`    |
| deletable     | Whether to show the delete button                                                                                                                                        | `boolean`                                                 | `true`    |
| capture       | Picture selection mode, the optional value is `camera` (directly adjust the camera)                                                                                      | `boolean \| string`                                       | -         |
| onPreview     | Callback when the preview picture is clicked                                                                                                                             | `(index: number) => void`                                 | -         |
| beforeUpload  | Callback function before file reading, return `false` to terminate file reading, support return `Promise`                                                                | `(file: File[]) => Promise<File[]> \| File[]`             | -         |
| upload        | Upload method, the input parameter is the file object that needs to be uploaded, after asynchronous processing, the upload result is returned                            | `(file: File) => Promise<FileItem>`                       | -         |
| onDelete      | Triggered when the successfully uploaded image is deleted, if it returns false, it means that it is prevented from being deleted, and it supports the return of Promise. | `(file: FileItem) => boolean \| Promise<boolean> \| void` | -         |
| children      | Custom upload button                                                                                                                                                     | `ReactNode`                                               | -         |

### CSS Variables

| Name        | Description                         | Default |
| ----------- | ----------------------------------- | ------- |
| --cell-size | The size of image and upload button | `80px`  |

## FileItem

| Name | Description                         | Type     | Default |
| ---- | ----------------------------------- | -------- | ------- |
| url  | The resource address of the picture | `string` | -       |
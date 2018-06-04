# luupeli-backend
[![Build Status](https://travis-ci.org/luupeli/luupeli-backend.svg?branch=master)](https://travis-ci.org/luupeli/luupeli-backend)

### Endpoints

Path | Method | Description
-----|------|------------
`/bones/` | GET | Returns an array of all bones.
`/bones/` | POST | Creates a new bone.
`/bones/:boneId` | GET | Gets a specific bone.
`/bones/:boneId` | PUT | Edits a Latin name and name. Images cannot be edited, because images add and delete by own methods.
`/bones/:boneId` | DELETE | Removes a specific bone and all images which are connected with it.
`/images/` | GET | Returns an array of all images.
`/images/` | POST | Creates a new image.
`/images/:imageId` | GET | Gets a specific image.
`/images/:imageId` | PUT | Edits difficulty and url. The bone cannot be edited.
`/images/:imageId` | DELETE | Removes a specific image and removes connect if the image is connected with bone.

#### Bone
##### POST Example
```
{
    "name": "reisiluu",
    "nameLatin": "ossis femoris",
    "images": ["5b15674e6ff3192a471571fa", "5b156d2af4d39b2db027f191"]
}
```

#### Image
##### POST Example
```
{
    "difficulty": "1",
    "url": "ossisfemoris.jpg",
    "bone": "5b152f647053790f4be55bc4"
}
```

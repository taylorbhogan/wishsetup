# wish
share your wishlist with your loved ones to help them communicate, and keep their claims a surprise to you.

## technology

### Design
designed using [figma](https://figma.com); view the design file [here](https://www.figma.com/file/1JnxKYqqK2hl6OQv1Fn3ZK/Wish-Mobile-Design-1?node-id=0%3A1).
- color palette: [materialDesign](https://material.io/design/color/the-color-system.html#tools-for-picking-colors)
  - yellow 300: ![#fff176](https://via.placeholder.com/15/fff176/000000?text=+) `#fff176`
  - yellow 600: ![#fdd835](https://via.placeholder.com/15/fdd835/000000?text=+) `#fdd835`
  - yellow 900: ![#f57f16](https://via.placeholder.com/15/f57f16/000000?text=+) `#f57f16`
  - blue 200: ![#8a9bee](https://via.placeholder.com/15/8a9bee/000000?text=+) `#8a9bee`
  - blue 400: ![#2c57d2](https://via.placeholder.com/15/2c57d2/000000?text=+) `#2c57d2`
  - blue 900: ![#000989](https://via.placeholder.com/15/000989/000000?text=+) `#000989`
- placeholder images for this README: [placeholder](https://placeholder.com/)
- illustrations: [unDraw](https://undraw.co)
- ui elements: [materialUi](https://mui.com)

### Database
[MongoDB](https://www.mongodb.com/)

## Database Schema
![Screen Shot 2022-04-02 at 8 35 20 PM](https://user-images.githubusercontent.com/79616733/161410240-bc0d4bc3-0876-42ef-9e7a-7cec93fe2d16.png)


### Users
| Field             | Data Type               | Constraints
| ---------------   | ---------------         | ---------------
| `id`              | `string`                | `not null`, `primary key`
| `name`            | `string`                | `not null`
| `email`           | `string`                | `not null`
| `hashedPassword`  | `string`                | `not null`
| `avatar`          | `string`                | 
| `groups`          | `array: [ ObjectId ]`   | `not null`

### Groups
| Field             | Data Type               | Constraints
| ---------------   | ---------------         | ---------------
| `id`              | `string`                | `not null`, `primary key`
| `name`            | `string`                | 
| `users`           | `array: [ ObjectId ]`   | `not null`

### Gifts
| Field             | Data Type               | Constraints
| ---------------   | ---------------         | ---------------
| `id`                | `string`                  | `not null`, `primary key`
| `name`              | `string`                  | `not null`
| `description`       | `string`                  |
| `wishedBy`          | `objectId`                | `not null`
| `isClaimed`         | `boolean`                 | `not null`, `default = false`
| `claimedBy`         | `objectId`                | 
| `url`               | `string`                  |


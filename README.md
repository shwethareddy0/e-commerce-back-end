# E-commerce Back End

## Description

E-commerce Back End is an application that provides APIs to create, update,delete and view the all the product with the associated categories and the tags.

This application uses the MySQL to store the database, Sequelize as an ORM application and the dotenv to use the environment to store the sensitive information of the user.

Here is a walkthrough [video]() demonstrating the functionality of the application.

### Features

- Easy to modify
- Provides APIs to view, add, update and delete the products, categories and tags.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Technologies Used](#technologies-used)
- [Credits](#credits)
- [License](#license)

## Installation

- Create a new repository on your GitHub account.
- Clone this repository.
- Run `npm i`
- Run `mysql -u root -p`
- Run `schema.sql`
- Run `npm run seed`
- Run `node server.js`
- Use Insominia or any REST API client to interact with the application.

## Usage

This project can be used in any Node.js environment.

Following is a code snippet of the application page.

Here it refers to the API PUT Route to update a category by its `id` value.

```Node.js

router.put("/:id", async (req, res) => {
  try {
        const updatedCategory = await Category.update(
      {
        category_name: req.body.category_name,
      },
      {
        where: {
          id: req.params.id,
        },
      }
    );
    res.status(200).json(updatedCategory);
  } catch (err) {
    res.status(400).json(err);
  }
});


```

## Technologies Used

- Node.js
- Express.js
- MySQL
- Sequelize
- Dotenv
- Insomnia
- Git
- GitHub

## Credits

- npmjs.com
- MDN / W3Schools

## License

This project is licensed under the [MIT](./LICENSE) license.

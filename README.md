## Usage

```rest_api

# Identifying resources and defining endpoints

# Example: User resource
# Endpoint: /users

## GET /users - Fetch all users
app.get('/users', (req, res) => {
  # Logic to fetch all users
  res.send('Get all users');
});

## POST /users - Create a new user
app.post('/users', (req, res) => {
  # Logic to create a new user
  res.send('Create a new user');
});

## GET /users/:userId - Fetch a specific user
app.get('/users/:userId', (req, res) => {
  const userId = req.params.userId;
  # Logic to fetch a specific user
  res.send(`Get user with ID: ${userId}`);
});

## PUT /users/:userId - Update a specific user
app.put('/users/:userId', (req, res) => {
  const userId = req.params.userId;
  #/ Logic to update a specific user
  res.send(`Update user with ID: ${userId}`);
});

## DELETE /users/:userId - Delete a specific user
app.delete('/users/:userId', (req, res) => {
  const userId = req.params.userId;
  # Logic to delete a specific user
  res.send(`Delete user with ID: ${userId}`);
});

## Utilising query parameters

# Example: Product resource
# Endpoint: /products

## GET /products - Fetch all products with optional filtering and pagination
app.get('/products', (req, res) => {
  const { category, page, limit } = req.query;
  // Logic to fetch products with optional filtering and pagination
  res.send(`Get products with category: ${category}, page: ${page}, limit: ${limit}`);
});

```

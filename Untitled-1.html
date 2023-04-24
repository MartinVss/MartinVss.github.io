const express = require('express');
const bodyParser = require('body-parser');
const mysql = require('mysql');

const app = express();
app.use(bodyParser.json());
app.use(bodyParser.urlencoded({ extended: true }));

// create MySQL connection
const connection = mysql.createConnection({
  host: 'localhost',
  user: 'root',
  password: 'password',
  database: 'toyshop'
});

// connect to MySQL
connection.connect(function(err) {
  if (err) {
    console.error('Error connecting to MySQL: ' + err.stack);
    return;
  }
  console.log('Connected to MySQL as id ' + connection.threadId);
});

// get all products
app.get('/products', function(req, res) {
  connection.query('SELECT * FROM products', function(error, results, fields) {
    if (error) throw error;
    res.json(results);
  });
});

// get product by id
app.get('/products/:id', function(req, res) {
  const productId = req.params.id;
  connection.query('SELECT * FROM products WHERE id = ?', [productId], function(error, results, fields) {
    if (error) throw error;
    res.json(results);
  });
});

// add new product
app.post('/products', function(req, res) {
  const product = req.body;
  connection.query('INSERT INTO products SET ?', product, function(error, results, fields) {
    if (error) throw error;
    res.json(results);
  });
});

// update product by id
app.put('/products/:id', function(req, res) {
  const productId = req.params.id;
  const product = req.body;
  connection.query('UPDATE products SET ? WHERE id = ?', [product, productId], function(error, results, fields) {
    if (error) throw error;
    res.json(results);
  });
});

// delete product by id
app.delete('/products/:id', function(req, res) {
  const productId = req.params.id;
  connection.query('DELETE FROM products WHERE id = ?', [productId], function(error, results, fields) {
    if (error) throw error;
    res.json(results);
  });
});

// start server
const server = app.listen(3000, function() {
  const host = server.address().address;
  const port = server.address().port;
  console.log('Server listening at http://%s:%s', host, port);
});

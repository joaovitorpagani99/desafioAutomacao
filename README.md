O script realizará as seguintes etapas:

### Login:

* Preenche as informações de login (usuário e senha) lidas de um arquivo CSV.
```
email_field = WebDriverWait(driver, 10).until(EC.presence_of_element_located((By.ID, "user-name")))
password_field = WebDriverWait(driver, 10).until(EC.presence_of_element_located((By.ID, "password")))
```
### Adição de Itens ao Carrinho:

* Adiciona produtos ao carrinho de compras. Os produtos são definidos no script.

```
add_button = WebDriverWait(driver, 10).until(EC.presence_of_element_located((By.XPATH, item.xpath)))
add_button.click()
time.sleep(WAIT_TIME)
```

### Checkout:

* Navega para o carrinho de compras e inicia o processo de checkout.
Informações do Usuário:

* Preenche as informações do usuário (nome, sobrenome, código postal) durante o checkout.

```
first_name_field = WebDriverWait(driver, 10).until(EC.presence_of_element_located((By.ID, "first-name")))
last_name_field = WebDriverWait(driver, 10).until(EC.presence_of_element_located((By.ID, "last-name")))
postal_code_field = WebDriverWait(driver, 10).until(EC.presence_of_element_located((By.ID, "postal-code")))
```

### Exibe o Total da Compra:

* Imprime o valor total da compra.

```
total = WebDriverWait(driver, 10).until(
    EC.presence_of_element_located((By.XPATH, '//*[@id="checkout_summary_container"]/div/div[2]/div[8]'))).text
```

### Produtos
* Os produtos a serem adicionados ao carrinho são definidos no script na função main(). Você pode modificar a lista de produtos conforme necessário.

### Customizações
* Sinta-se à vontade para personalizar o script de acordo com suas necessidades, como adicionar mais produtos, modificar informações de usuário, etc.

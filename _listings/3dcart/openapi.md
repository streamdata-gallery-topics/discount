swagger: "2.0"
x-collection-name: 3dcart
x-complete: 1
info:
  title: _3dCartWebAPI
  version: 1.0.0
host: apirest.3dcart.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /3dCartWebAPI/v1/Products/{catalogid}/Discount:
    post:
      summary: Adds a new discount to the system
      description: Adds a new discount to the system.
      operationId: Products_Post
      x-api-path-slug: 3dcartwebapiv1productscatalogiddiscount-post
      parameters:
      - in: path
        name: catalogid
        description: Catalog ID
      - in: body
        name: discount
        description: A Json or XML object containing the new discount
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: PrivateKey
        description: PrivateKey
      - in: header
        name: SecureURL
        description: SecureURL
      - in: header
        name: Token
        description: Token
      responses:
        200:
          description: OK
      tags:
      - S
      - New
      - Discount
      - To
      - System
    get:
      summary: Get the discounts from a specific Product
      description: Get the discounts from a specific product.
      operationId: Products_GetAllProductDiscount
      x-api-path-slug: 3dcartwebapiv1productscatalogiddiscount-get
      parameters:
      - in: path
        name: catalogid
        description: Catalog ID
      - in: query
        name: limit
        description: Maximum number of items that can be returned
      - in: query
        name: offset
        description: Starting point for the return data
      - in: header
        name: PrivateKey
        description: PrivateKey
      - in: header
        name: SecureURL
        description: SecureURL
      - in: header
        name: Token
        description: Token
      responses:
        200:
          description: OK
      tags:
      - Discounts
      - From
      - Specific
      - Product
    put:
      summary: Updates a collection of discounts from a specific Product
      description: Updates a collection of discounts from a specific product.
      operationId: Products_Update
      x-api-path-slug: 3dcartwebapiv1productscatalogiddiscount-put
      parameters:
      - in: path
        name: catalogid
        description: CatalogID
      - in: body
        name: discounts
        description: A Json or XML object containing the new discount
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: PrivateKey
        description: PrivateKey
      - in: header
        name: SecureURL
        description: SecureURL
      - in: header
        name: Token
        description: Token
      responses:
        200:
          description: OK
      tags:
      - S
      - Collection
      - Of
      - Discounts
      - From
      - Specific
      - Product
  /3dCartWebAPI/v1/Products/{catalogid}/Discount/{discountid}:
    put:
      summary: Updates a specific discount from a specific Product
      description: Updates a specific discount from a specific product.
      operationId: Products_Update
      x-api-path-slug: 3dcartwebapiv1productscatalogiddiscountdiscountid-put
      parameters:
      - in: path
        name: catalogid
        description: CatalogID
      - in: body
        name: discount
        description: A Json or XML object containing the new discounts
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: discountid
        description: DiscountID
      - in: header
        name: PrivateKey
        description: PrivateKey
      - in: header
        name: SecureURL
        description: SecureURL
      - in: header
        name: Token
        description: Token
      responses:
        200:
          description: OK
      tags:
      - S
      - Specific
      - Discount
      - From
      - Specific
      - Product
# GraphQLRestaurants

## Learn how to post, edit, delete and read data on GraphQL

Copy these files onto your machine in a node file.
Start GraphQL by typing "node index.js" into your terminal.
You will find GraphQL running on " http://localhost:5500/graphql "
These preset commands will let you easily edit the data:



mutation editrestaurants($idd: Int = 3, $name: String = "Denny's" ) {
  editrestaurant(id: $idd, name: $name) {
    name
    description
  }
}

mutation setrestaurants {
  setrestaurant(input: {
    name: "Del Taco",
    description: "Mexican Fast Food",
  }) {
    name
    description
  }
}

mutation deleterestaurants($iid: Int = 3) {
  deleterestaurant(id: $iid) {
    ok
  }
}

query getrestaurants {
  restaurants {
    name
    description
    dishes {
      name
      price
    }
  }
}

query getsinglerestaurant ($iid: Int = 1) {
    restaurant(id:$iid){
    name
    description
    dishes {
      name
      price
    }
  }
}

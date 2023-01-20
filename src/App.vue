<template>
  <section>
    <header>
      <h1>Active Users</h1>
    </header>
    <user-data @add-user="addUser"></user-data>
    <ul>
      <active-user
        v-for="user in users"
        :key="user.id"
        :name="user.name"
        :age="user.age"
      ></active-user>
    </ul>
  </section>
</template>

<script>
export default {
  data() {
    return {
      users: [
        {
          id: "dato",
          name: "dato purceladze",
          age: 24,
        },
        {
          id: "ana",
          name: "ana khundadze",
          age: 23,
        },
      ],
    };
  },
  methods: {
    addUser(name, age) {
      const newUser = {
        id: new Date().toISOString(),
        name: name,
        age: age,
      };
      this.users.push(newUser);
    },
  },
};
</script>

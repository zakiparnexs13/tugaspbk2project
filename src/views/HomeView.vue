<template>
  <div class="container">
    <div class="header">
      <h1>My Portfolio</h1>
      <p>Welcome to my portfolio website</p>
    </div>

    <div class="projects">
      <div class="project" v-for="project in projects" :key="project.id">
        <h2>{{ project.title }}</h2>
        <p>{{ project.description }}</p>
        <a :href="project.link" class="btn">View Details</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          id: 1,
          title: 'Project 1',
          description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed suscipit placerat tortor at elementum.',
          link: '#'
        },
        {
          id: 2,
          title: 'Project 2',
          description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed suscipit placerat tortor at elementum.',
          link: '#'
        },
        {
          id: 3,
          title: 'Project 3',
          description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed suscipit placerat tortor at elementum.',
          link: '#'
        }
      ]
    };
  }
};
</script>

<style>
.container {
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
}

.header {
  background-color: #4f46e5;
  color: #fff;
  padding: 20px;
  text-align: center;
}

.header h1 {
  font-size: 32px;
}

.projects {
  display: grid;
  grid-gap: 20px;
}

.project {
  background-color: #f9fafb;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  padding: 20px;
}

.project h2 {
  font-size: 24px;
  margin-bottom: 10px;
}

.project p {
  margin-bottom: 10px;
}

.btn {
  background-color: #4f46e5;
  color: #fff;
  padding: 10px 20px;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.btn:hover {
  background-color: #4039c3;
}
</style>

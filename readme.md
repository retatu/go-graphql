```
query findCategories {
  categories{
    id
    name
    description
    course{
      name
      description
      chapters{
        name
      }
    }
  }
}


query findCourses{
  courses {
    id
    name
    category{
      name
      description
    }
    chapters{
      name
    }
  }
}


query findChapters {
  chapters {
    id
    name
    course{
      name
      description
    }
  }
}


mutation createCategory {
  createCategory(input: { name: "MR", description: "Matheus Rehbein" }) {
    id
    name
    description
  }
}


mutation createCourse {
  createCourse(
    input: {
      name: "Course"
      description: "Course 1"
      categoryId: "T5577006791947779410"
    }
  ) {
    id
    name
    description
    category {
      id
      description
    }
  }
}


mutation createChapter{
  createChapter(
  input: {
    name: "Chapter", 
    courseId: "T8674665223082153551"
  })
  {
    id,
    name,
  }
}```

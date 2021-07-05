<template>
  <div class="activities">
    <h1>Physical Therapy Activites</h1>
    <h3>Enter a new Exericse</h3>
    <div class="form-group row" id="newExercise">
      <div class="col-sm-3">
        <input
          type="text"
          class="form-control"
          v-model="newActivity.exercise"
          placeholder="Exercise"
        />
      </div>
      <div class="col-sm-2">
        <input
          type="text"
          class="form-control"
          v-model="newActivity.date"
          placeholder="MM/DD/YYYY"
        />
      </div>
      <div class="col-sm-1">
        <input
          type="number"
          class="form-control"
          v-model="newActivity.reps"
          placeholder="Reps"
        />
      </div>
      <div class="col-sm-1">
        <input
          type="number"
          class="form-control"
          v-model="newActivity.weight"
          placeholder="Weight/Resist"
        />
      </div>
      <div class="col-sm-2">
        <input
          type="number"
          class="form-control"
          v-model="newActivity.time"
          placeholder="Time in Mins"
        />
      </div>
      <button
        class="btn btn-success col-sm-2"
        v-on:click="addActivity(newActivity, activities)"
      >
        Enter Exercise
      </button>
    </div>

    <div id="exercises">
      <table>
        <thead>
          <tr>
            <th>Exercise</th>
            <th>Date</th>
            <th>Reps</th>
            <th>Weight</th>
            <th>Time</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="(activity, index) in activities" :key="index">
            <td>{{ activity.exercise }}</td>
            <td>{{ activity.date }}</td>
            <td>{{ activity.reps }}</td>
            <td>{{ activity.weight }}</td>
            <td>{{ activity.time }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
import exerciseData from "../assets/exerciseData.js";

export default {
  data: () => {
    return {
      exercises: [],
      activities: exerciseData,
      exercise_filter: "",
      newActivity: {}
    };
  },
  methods: {
    addActivity: (newActivity, activities) => {
      activities.push(newActivity);
      newActivity.exercise = "";
      newActivity.date = "";
      newActivity.reps = "";
      newActivity.weight = "";
      newActivity.time = "";
    }
  }
};
</script>

<style scoped>
.activities {
  text-align: left;
}

h1 {
  text-align: center;
}

table {
  border-collapse: collapse;
  width: 90vw;
  /* margin-left: 5vw; */
}

td,
th {
  border: 1px solid;
  padding: 2rem;
}

#newExercise {
  margin-bottom: 15px;
}

.activities {
  width: 90vw;
  margin-left: 5vw;
}
</style>

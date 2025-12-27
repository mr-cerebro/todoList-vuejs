<template>
  <div class="min-h-screen bg-base-200 flex items-center justify center p-4">
    <div class="card w-full max-w-md bg base-100 shadow-xl">
      <div class="card-body">
        <h2 class="card-title text-2l font-bold mt-4">To-Do List</h2>

        <div class="flex gap-2 mb-6">
          <input
            v-model="newTask"
            @keyup.enter="addTask"
            type="text"
            placeholder="Add a new task..."
            class="input input-bordered w-full"
          />
          <button @click="addTask" class="btn btn-primary">Add</button>
        </div>

        <div class="space-y-3">
          <div
            v-for="task in taks"
            :key="task.id"
            class="flex items-center justify-between bg-base-200 p-3 rounded-lg"
          >
            <div class="flex items-center gap-3">
              <input type="checkbox" v-model="task.completed" class="checkbox checkbox-success" />
              <span :class="{ 'line-through opacity-50': task.completed }">{{ task.text }}</span>
            </div>
            <button @click="deleteTask(task.id)" class="btn btn-ghost btn-xs text-error">
              Delete
            </button>
          </div>
        </div>

        <div class="divider"></div>
        <div class="flex justify-between txt-sm opacity-70">
          <span>Total {{ totalTasks }}</span>
          <span>{{ completedTasks }}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { computed, ref } from 'vue'

const newTask = ref('')
const taks = ref([
  {
    id: 1,
    text: 'Learn Vue 3',
    completed: false,
  },
  {
    id: 2,
    text: 'Configure daisyUI',
    completed: true,
  },
])

// Add a new task
const addTask = () => {
  if (newTask.value.trim() === '') return
  taks.value.push({
    id: Date.new(),
    text: newTask.value,
    completed: false,
  })
  newTask.value = ''
}

// Delete task
const deleteTask = (id) => {
  taks.value = taks.value.filter(task => task.id !== id)
}

// Statistics
const totalTasks = computed(() => taks.value.length)
const completedTasks = computed(() => taks.value.filter(t => t.completed).length)
</script>

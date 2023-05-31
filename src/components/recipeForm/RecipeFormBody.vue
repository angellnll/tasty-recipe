<template>
  <li class="list-group-item">
    <form @submit.prevent="addNewRecipe">
      <!-- General Information Start -->
      <div>
        <p class="my-3 fs-5 fw-semibold">General Information</p>
        <div>
          <!-- Image Start -->
          <div class="mb-3">
            <base-input
              type="file"
              identity="recipeImage"
              label="Photo Recipe"
            ></base-input>
          </div>
          <!-- Image End -->

          <!-- Recipe Title Start -->
          <div class="mb-3">
            <base-input
              type="text"
              id="recipeTitle"
              placeholder="Give your recipe a title"
              label="Recipe Title"
            ></base-input>
          </div>
          <!-- Recipe Title  End -->

          <!-- Recipe Description Start -->
          <div class="mb-3">
            <base-text-area
              identity="recipeDescription"
              label="Description"
              placeholder="Share story behind recipe and what is make it special"
            ></base-text-area>
          </div>
          <!-- Recipe Description End -->

          <!-- Recipe Cateogry Start -->
          <div class="mb-3">
            <base-select
              :data="['Breakfast', 'Lunch', 'Dinner', 'Meals', 'Snacks']"
            ></base-select>
          </div>
          <!-- Recipe Category End -->
        </div>
      </div>
      <!-- General Information End -->

      <!-- Time Setting Start -->
      <div class="border-top py-1">
        <p class="my-3 fs-5 fw-semibold">Time Setting</p>
        <div>
          <div class="mb-3">
            <base-input
              type="number"
              identity="prepTime"
              placeholder="0"
              label="Prep Time"
            ></base-input>
          </div>
          <div class="mb-3">
            <base-input
              type="number"
              identity="cookTime"
              placeholder="0"
              label="Cook Time"
            ></base-input>
          </div>
          <div class="mb-3">
            <base-input
              type="number"
              identity="totalTime"
              placeholder="0"
              label="Total Time"
            ></base-input>
          </div>
        </div>
      </div>
      <!-- Time Setting End -->

      <!-- Ingredients Start -->
      <div class="border-top py-1">
        <p class="my-3 fs-5 fw-semibold">Ingredients</p>
        <p>
          Enter one ingredient per line. Include the quantity (i.e. cups,
          tablespoons) and any special preparation (i.e. sifted, softened,
          chopped). Use optional headers to organize the different parts of the
          recipe (i.e. Cake, Frosting, Dressing).
        </p>
        <div>
          <div class="mb-3 row">
            <div class="col-lg-11 col-11">
              <base-input
                type="text"
                identity="ingredient"
                placeholder="Ex : 1 cup sugar"
              ></base-input>
            </div>
            <div
              class="col-lg-1 col-1 col-form-label align-self-end delete-ingredient"
              style="color: #cb3a31"
            >
              <i class="fa-regular fa-trash-can px-1"></i
              ><span class="d-none d-md-inline">Delete</span>
            </div>
          </div>
        </div>
        <base-button class="new-ingredient-btn px-3 py-2"
          ><i class="fa-solid fa-plus me-2"></i>Add More</base-button
        >
      </div>
      <!-- Ingredients End -->

      <!-- Direction Start -->
      <div class="border-top my-3">
        <p class="my-3 fs-5 fw-semibold">Directions</p>
        <p>
          Explain how to make your recipe, including oven temperatures, baking
          or cooking times, and pan sizes, etc. Use optional headers to organize
          the different parts of the recipe
        </p>
        <div>
          <div class="mb-3 row">
            <div class="col-lg-11 col-11">
              <base-input
                type="text"
                identity="direction"
                placeholder="Ex : 1 cup sugar"
              ></base-input>
            </div>
            <div
              class="col-lg-1 col-1 col-form-label align-self-end delete-ingredient"
              style="color: #cb3a31"
            >
              <i class="fa-regular fa-trash-can px-1"></i
              ><span class="d-none d-md-inline">Delete</span>
            </div>
          </div>
        </div>
        <base-button class="new-ingredient-btn px-3 py-2"
          ><i class="fa-solid fa-plus me-2"></i>Add More</base-button
        >
      </div>
      <!-- Direction End -->

      <!-- Submit Button Start -->
      <div class="border-top py-3 d-flex my-4 justify-content-end">
        <div @clickButton="cancelRecipe" class="cancel-btn px-3 py-2 me-1">
          Cancel
        </div>
        <base-button class="submit-recipe-btn px-3 py-2 ms-1"
          >Submit</base-button
        >
      </div>
      <!-- Submit Button End -->
    </form>
  </li>
</template>

<script setup>
import BaseInput from "../ui/BaseInput.vue";
import BaseTextArea from "../ui/BaseTextArea.vue";
import BaseSelect from "../ui/BaseSelect.vue";
import BaseButton from "../ui/BaseButton.vue";
</script>
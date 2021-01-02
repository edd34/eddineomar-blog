<template>
  <form>
    <!-- Name -->
    <div class="field">
      <label class="label is-medium">Nom</label>
      <div class="control has-icons-left">
        <input class="input is-medium" type="text" placeholder="Jean Michel" />
        <span class="icon is-small is-left">
          <font-awesome-icon icon="user" />
        </span>
      </div>
    </div>
    <!-- Email -->
    <div class="field">
      <label class="label is-medium">Email</label>
      <div class="control has-icons-left">
        <input
          class="input is-medium"
          type="email"
          placeholder="vous@email.fr"
        />
        <span class="icon is-small is-left">
          <font-awesome-icon icon="envelope" />
        </span>
      </div>
    </div>
    <!-- Subject -->
    <div class="field">
      <label class="label is-medium">Objet</label>
      <div class="control has-icons-left">
        <input
          class="input is-medium"
          type="text"
          placeholder="De quoi s'agit-il ?"
        />
        <span class="icon is-small is-left">
          <font-awesome-icon icon="briefcase" />
        </span>
      </div>
    </div>
    <!-- Message -->
    <div class="field">
      <label class="label is-medium">Message</label>
      <div class="control">
        <textarea
          class="textarea"
          placeholder="Un peu plus de détail concernant votre question, commentaire, requête etc.."
          rows="8"
        ></textarea>
      </div>
    </div>
    <div class="control">
      <button class="button is-primary">
        Envoyer
      </button>
    </div>
  </form>
</template>

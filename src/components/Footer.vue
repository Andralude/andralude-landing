<template>
  <!--Footer-->
  <footer class="bg-white">
    <div class="container mx-auto px-8 py-8 flex justify-center gap-2">
      <p class="text-gray-500">
        © <a class="text-pink-900 cursor-pointer" :onClick="scrollToHeader">Andralude</a> 2021-{{ year }}
      </p>
      <div class="h-6 w-0.5 bg-gray-300 rounded-full" />
      <p class="text-gray-500"><a @click="showModal" class="text-pink-900 cursor-pointer">Mentions légales</a></p>
    </div>
  </footer>
  <Modal v-show="isModalVisible" @close="closeModal">
    <template v-slot:title>
      Mentions Légales
    </template>

    <template v-slot:body>
      <p class="text-black whitespace-pre-line">
        Directeur de la publication : Éric PAILHAREY
        <br />Directeur technique : Axel LOPEZ
        <br />
        <br /><b>Andralude</b>
        <br />Andragos
        <br />1 traverse des Brucs
        <br />06560 Valbonne
        <br />France
        <br />tél. 06 45 72 00 02
        <br />eric.pailharey@andralude.com
        <br />
        <br /><b>Hébergeur</b>
        <br />Nartium
        <br />2 rue du port
        <br />91450 Soisy sur Seine
        <br />France
        <br />
        <br />En utilisant le site, l'utilisateur reconnaît avoir pris connaissance de ces conditions et les avoir
        acceptées.
        <br />Celles-ci pourront être modifiées à tout moment et sans préavis par Andralude. Par ailleurs, l'utilisateur reconnaît avoir été informé que le présent site est accessible 24 heures sur 24 et 7 jours sur 7, à
        l'exception des cas de force majeure, difficultés informatiques, difficultés liées à la structure des réseaux de communication ou difficultés techniques. Pour des raisons de maintenance, Andralude pourra interrompre le
        site et s'efforcera d'en avertir préalablement les utilisateurs.
        <br />
        <br /><b>Liens vers des tiers</b>
        <br />Les liens hypertextes mis en place dans le cadre du présent site en direction d'autres ressources
        présentes sur le réseau Internet et, notamment, vers les partenaires, sont clairement identifiés et font l'objet d'une information et/ou d'une autorisation préalable des sites pointés.
        <br />Andralude s'engage à faire cesser les liens hypertextes à la première demande des entreprises à qui
        appartiennent ces sites.
        <br />Les liens hypertextes en direction d'autres ressources présentes sur le réseau Internet ne sauraient
        engager la responsabilité d'Andralude
        <br />
        <br /><b>Déclaration</b>
        <br />Le traitement automatisé des informations personnelles réalisé à partir du site a fait l'objet d'une
        déclaration auprès de la Commission Nationale de l'Informatique et des Libertés. En conformité avec les dispositions
        de la loi n°78-17 du 6 janvier 1978 modifiée par la loi 2004-801 du 6 août 2004 relative à l'informatique, aux fichiers et aux libertés.
        <br />Par « informations personnelles », il faut entendre toute information qui permet d'identifier une
        personne. Il s'agira le plus souvent d'un nom, d'une adresse, d'un numéro de téléphone ou d'une adresse électronique.
        <br />Vous disposez d'un droit d'accès, de modification, de rectification et de suppression des données qui vousconcernent (art.34).
        <br />
        <br /><b>Propriété intellectuelle</b>
        <br />Tout le contenu du site, les graphismes, images, textes, logos ainsi que leur mise en forme sont la
        propriété exclusive d'Andralude à l'exception des marques, logos ou contenus appartenant à d'autres sociétés
        partenaires.
        <br />Toute représentation totale ou partielle de ce site par quelque procédé que ce soit, sans l'autorisation expresse d'Andralude est interdite et constituerait une contrefaçon sanctionnée par les articles L.335-2 et suivant le code de la propriété intellectuelle.
        <br />Toute reproduction totale ou partielle des marques ou logos d'Andralude ou de ses partenaires effectuée à
        partir des éléments du site sans l'autorisation expresse d'Andralude ou du propriétaire du logo ou de la marque
        est prohibée selon le code de la propriété intellectuelle.
        <br />Le visiteur est informé que, lors de ses visites sur le site, un cookie peut s'installer automatiquement
        sur son navigateur. Le cookie est un bloc de données qui ne permet pas d'identifier le visiteur ; en revanche, il enregistre des informations relatives à la navigation de votre ordinateur sur notre site (les
        pages consultées, la date et l'heure de la consultation, etc.) que nous pourrons lire lors de vos visites
        ultérieures.
        <br />
        <br /><b>Cookies</b>
        <br />Il vous est possible de détecter l'existence de ces « cookies » et, le cas échéant, de les supprimer.
        <br />Il vous est également possible de vous opposer à l'enregistrement de cookies en désactivant cette fonction
        de votre navigateur dans les préférences de celui-ci.
        <br />
        <br /><b>Attribution de juridiction</b>
        <br />En cas de litige entre Andralude et tout tiers du fait du présent site, la juridiction compétente sera
        celle dont ressort le siège social d'Andralude
      </p>
    </template>
  </Modal>
</template>

<script setup lang="ts">
import Modal from './Modal.vue';
</script>

<script lang="ts">

export default {
  name: 'Footer',
  data() {
    return {
      year: new Date().getFullYear(),
      isModalVisible: false
    }
  },
  methods: {
    showModal() {
      this.isModalVisible = true;
      const body = document.getElementById("body");
      body!.style.overflow = "hidden";
    },
    closeModal() {
      this.isModalVisible = false;
      const body = document.getElementById("body");
      body!.style.overflow = "auto";
    },
    scrollToHeader() {
      const hero = document.getElementById("hero");
      if (hero) {
        hero.scrollIntoView({ behavior: "smooth" });
      }
    }
  },
};
</script>
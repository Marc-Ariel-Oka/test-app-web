<script>
import Navbar from "./components/Navbar.vue";
import CardBalanceViewer from "./components/CardBalanceViewer.vue";
import CardMenu from "./components/CardMenu.vue";
import Bottombar from "./components/Bottombar.vue";

export default {
  components: {
    Navbar,
    CardBalanceViewer,
    CardMenu,
    Bottombar,
  },
  data() {
    return {

      balances: [
        { img: "Functional_UI - ic_Donation 1-1.png", name: "Compte principal" },
        { img: "Functional_UI - ic_Donation 1.png", name: "Solde principal" },
      ],

      banner: [
        { img: "Group 1365.png", name: "Recharger" },
        { img: "Content image.png", name: "Acheter un pass" },
        { img: "Thumbnail.png", name: "Transfert d'argent" },
        { img: "Thumbnail-1.png", name: "Paiement Marchand" },
      ],

      services: [
        { img: "atom_quickicon_deals.png", name: "Promo" },
        { img: "atom_quickicon_ozen.png", name: "O'zen" },
        { img: "atom_secondaryicon_line_outlined copie.png", name: "Ma SIM" },
        { img: "atom_secondaryicon_mylives.png", name: "Live Streaming" },
      ],

      payer: [
        { img: "SOS.png", name: "SOS" },
        { img: "content.png", name: "Transfer credit" },
        { img: "atom_quickicon_paybill.png", name: "Facture Orange" },
        { img: "atom_secondaryicon_line_outlined.png", name: "Gerer ma Sim" },
      ],

      achats: [
        { img: "atom_secondaryicon_myservices.png ", name: "Mes Services" },
        { img: "atom_secondaryicon_mytickets.png", name: "Tickets" }
      ],

      aide: [
        { img: "atom_secondaryicon_faq.png", name: "Assistance en ligne" },
        { img: "atom_secondaryicon_bookspot.png", name: "Trouver une agence" },
        { img: "5cc4f357d335d4fda0c6838cf2eb883e-removebg-preview.png", name: "Pharmacie de garde" },
        { img: "atom_quickicon_parainnage.png", name: "Parrainage" },
      ],
    };
  },
};
</script>

<template>
  <div class="m-2">
    <Navbar />
    <div class="mt-5">
      <h1 class="fs-5 text-welcome">Bienvenue, +225 0709925266</h1>

      <!-- balance viewer -->
      <div class="mt-3 row">
        <div class="col-6" v-for="row in balances">
          <CardBalanceViewer :img="row.img" :name="row.name" />
        </div>
      </div>
      <!-- fin balance viewer -->

      <div class="mt-4 row gx-2">
        <div class="col-3" v-for="row in banner">
          <CardMenu :img="row.img" :name="row.name" />
        </div>
      </div>

      <!-- services -->
      <div class="mt-4 px-2">
        <h2 class="fs-5 mb-3" style="font-weight: 700">Services</h2>
        <div class="row gx-1">
          <div class="col-6">
            <img src="./assets/icons/Illustration.png" class="object-contain" alt="" />
          </div>
          <div class="col-6">
            <div class="row gy-3 gx-3">
              <div class="col-6" v-for="row in services">
                <CardMenu :img="row.img" :name="row.name" :isService="true" />
              </div>
            </div>
          </div>
        </div>
      </div>
      <!-- fin services -->

      <!-- payer & transfer -->
      <div class="mt-4">
        <h3 class="fs-5 mb-3" style="font-weight: 700">Payer & Transferer</h3>
        <div class="row gx-3">
          <div class="col-3" v-for="row in payer">
            <CardMenu :img="row.img" :name="row.name" />
          </div>
        </div>
      </div>
      <!-- fin payer & transfer -->

      <!-- achats -->
      <div style="margin-top: 7rem">
        <h3 class="fs-5 mb-3" style="font-weight: 700">Mes achats</h3>
        <div class="row gx-3">
          <div class="col-3" v-for="row in achats">
            <CardMenu :img="row.img" :name="row.name" />
          </div>
        </div>
      </div>
      <!-- fin achats -->

      <!-- payer & transfer -->
      <div class="mt-4 mb-4">
        <h3 class="fs-5 mb-3" style="font-weight: 700">Besoin d'aide ?</h3>
        <div class="row gx-3">
          <div class="col-3" v-for="row in aide">
            <CardMenu :img="row.img" :name="row.name" />
          </div>
        </div>
      </div>
      <!-- fin payer & transfer -->
    </div>
  </div>
  <Bottombar />
</template>

<style scoped>
.text-welcome {
  font-weight: 700;
}
</style>

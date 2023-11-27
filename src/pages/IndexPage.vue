<template>
  <q-page class="">
    <div class="bg">
      <div class="">
        <div class="" style="max-width: 100%">
          <div class="q-px-lg align-left">
            <q-tabs
              v-model="tab"
              class="text-grey-7 flat"
              active-color="primary"
              indicator-color="primary"
              align="left"
            >
              <q-tab class="q-px-xl" name="Sales" label="Sales"></q-tab>
              <q-tab
                class="q-px-xl"
                name="Collections"
                label="Collections"
              ></q-tab>
              <q-tab class="q-px-xl" name="Stock" label="Stock"></q-tab>
              <q-tab class="q-px-xl" name="MY KPIs" label="MY KPIs"></q-tab>
            </q-tabs>

            <q-tab-panels v-model="tab" animated class="tab-bg">
              <q-tab-panel name="Sales">
                <div class="q-mt-md">
                  <div class="row">
                    <div class="col-7 q-pr-md">
                      <div class="bg-white q-pa-md text-h6 poa shadow-3">
                        <div>Product Sold</div>
                        <div>
                          <ProductSold></ProductSold>
                        </div>
                      </div>
                    </div>

                    <div class="col-5 q-pl-md">
                      <div class="bg-white q-pa-md text-h6 srs shadow-3">
                        <div>Sales of SR</div>
                        <div class="q-mt-md">
                          <SrSales></SrSales>
                        </div>
                      </div>
                    </div>
                  </div>
                  <div class="q-mt-md">
                    <div class="row">
                      <div class="col-4 q-pr-md">
                        <div class="bg-white q-pa-md text-h6 tsp shadow-3">
                          <div>Top Sold Product</div>
                          <div class="flex flex-center">
                            <TopSoldProduct></TopSoldProduct>
                          </div>
                        </div>
                      </div>
                      <div class="col-3 q-pl-md q-pr-md">
                        <div class="row shop_sr justify-between">
                          <div
                            class="tsr col-12 q-mb-md bg-white flex flex-center shadow-3"
                          >
                            <div class="row">
                              <div
                                class="col-12 text-subtitle1 text-weight-bold text-center"
                              >
                                Total SR
                              </div>
                              <div
                                class="q-mt-md text-red text-h4 text-weight-bold col-12 text-center"
                              >
                                10
                              </div>
                            </div>
                          </div>
                          <div
                            class="ts col-12 bg-white flex flex-center shadow-3"
                          >
                            <div class="row">
                              <div
                                class="col-12 text-subtitle1 text-weight-bold text-center"
                              >
                                Total Outlet
                              </div>
                              <div
                                class="q-mt-md text-green text-weight-bold text-h4 text-weight-bold col-12 text-center"
                              >
                                2500
                              </div>
                            </div>
                          </div>
                        </div>
                      </div>
                      <div class="col-5 q-pl-md">
                        <div class="bg-white q-pa-md text-h6 cc shadow-3">
                          <div>Cash Collection</div>
                          <div>
                            <CashCollection></CashCollection>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </q-tab-panel>

              <q-tab-panel name="Collections">
                <div class="q-mt-md">
                  <div class="row">
                    <div class="col-3 q-pr-md">
                      <div class="tms shadow-3 bg-white column flex-center">
                        <div style="color: #102a43" class="text-h6">
                          Monthly Sales Balance
                        </div>
                        <div class="text-h5 text-green text-weight-medium">
                          ৳ 2586500
                        </div>
                      </div>
                    </div>
                    <div class="col-3 q-pr-md">
                      <div class="tms shadow-3 bg-white column flex-center">
                        <div style="color: #102a43" class="text-h6">
                          Monthly Receivable Balance
                        </div>
                        <div class="text-h5 text-red text-weight-medium">
                          ৳ 586500
                        </div>
                      </div>
                    </div>
                    <div class="col-3 q-pr-md">
                      <div class="tms shadow-3 bg-white column flex-center">
                        <div style="color: #102a43" class="text-h6">
                          Monthly Expenses
                        </div>
                        <div class="text-h5 text-red text-weight-medium">
                          ৳ 1856500
                        </div>
                      </div>
                    </div>
                    <div class="col-3 q-pr-md">
                      <div class="tms shadow-3 bg-white column flex-center">
                        <div style="color: #102a43" class="text-h6">
                          Monthly Revenue
                        </div>
                        <div class="text-h5 text-green text-weight-medium">
                          ৳ 205000
                        </div>
                      </div>
                    </div>
                  </div>
                  <div class="q-mt-lg">
                    <div class="row">
                      <div class="col-12 shadow-3 q-pr-md">
                        <div class="bg-white q-pa-md text-h6 tso">
                          <div>Monthly Sales and Receivable</div>
                          <div>
                            <SalesAndReceivable></SalesAndReceivable>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </q-tab-panel>

              <q-tab-panel name="Stock">
                <div class="q-mt-md">
                  <div class="row">
                    <div class="col-7 q-pr-md">
                      <div class="bg-white q-pa-md text-h6 bap shadow-3">
                        <div>Brandwise Available different products</div>
                        <div class="q-mt-md">
                          <AvailableProducts></AvailableProducts>
                        </div>
                      </div>
                    </div>
                    <div class="col-5 q-pr-md">
                      <div class="bg-white q-pa-md text-h6 map shadow-3">
                        <div class="row">
                          <div class="col-6 bdmap">
                            <div class="text-center">User By district</div>
                            <div class="q-pl-md">
                              <q-img width="200px" src="../assets/bdmap.png" />
                            </div>
                          </div>
                          <div class="col-6 top_district">
                            <div class="text-center">Top 5 Districts</div>
                            <div>
                              <TopDistrict></TopDistrict>
                            </div>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                  <div class="q-mt-md">
                    <div class="row">
                      <div class="col-6 q-pr-md">
                        <div class="bg-white q-pa-md text-h6 npi shadow-3">
                          <div>New Purchased Items</div>
                          <div class="q-mt-sm">
                            <NewPurchased></NewPurchased>
                          </div>
                        </div>
                      </div>
                      <div class="col-6 q-pr-md">
                        <div class="bg-white q-pa-md text-h6 pp shadow-3">
                          <div>Product Prices</div>
                          <div class="align-left">
                            <q-tabs
                              v-model="tab2"
                              dense
                              active-color="primary"
                              indicator-color="primary"
                            >
                              <q-tab name="Axe" label="Axe" />
                              <q-tab name="Dove" label="Dove" />
                              <q-tab name="Persil" label="Persil" />
                              <q-tab name="Comfort" label="Comfort" />
                              <q-tab name="Simple" label="Simple" />
                              <q-tab name="Tresemme" label="Tresemme" />
                              <q-tab name="Camay" label="Camay" />
                              <q-tab name="Bru" label="Bru" />
                              <q-tab name="Pears" label="Pears" />
                            </q-tabs>

                            <q-tab-panels v-model="tab2">
                              <q-tab-panel name="Axe">
                                <div class="q-mt-md"><AxePrice></AxePrice></div>
                              </q-tab-panel>
                              <q-tab-panel name="Dove">
                                <div class="q-mt-md">
                                  <DovePrice></DovePrice>
                                </div>
                              </q-tab-panel>
                              <q-tab-panel name="Persil">
                                <div class="q-mt-md">
                                  <PersilPrice></PersilPrice>
                                </div>
                              </q-tab-panel>
                              <q-tab-panel name="Comfort"
                                ><div class="q-mt-md">
                                  <ComfortPrice></ComfortPrice></div
                              ></q-tab-panel>
                              <q-tab-panel name="Simple"
                                ><div class="q-mt-md">
                                  <SimplePrice></SimplePrice>
                                </div>
                              </q-tab-panel>
                              <q-tab-panel name="Tresemme"
                                ><div class="q-mt-md">
                                  <TresemmePrice></TresemmePrice></div
                              ></q-tab-panel>
                              <q-tab-panel name="Camay"
                                ><div class="q-mt-md">
                                  <CamayPrice></CamayPrice></div
                              ></q-tab-panel>
                              <q-tab-panel name="Bru"
                                ><div class="q-mt-md">
                                  <BruPrice></BruPrice></div
                              ></q-tab-panel>
                              <q-tab-panel name="Pears"
                                ><div class="q-mt-md">
                                  <PearsPrice></PearsPrice></div
                              ></q-tab-panel>
                            </q-tab-panels>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </q-tab-panel>
              <q-tab-panel name="MY_KPIs">
                <div class="text-h6">MY KPIs</div>
                <div class="row flex flex-center">
                  <div
                    class="col-3 q-pa-md form shadow-2 text-white rounded-borders"
                  >
                    <div class="text-h5 text-center q-my-md">Claim form</div>
                    <div class="form-input q-px-sm">
                      <div>
                        <q-input
                          v-model="form.claim_title"
                          label="Claim title"
                          dark
                          label-color="white"
                          color="white"
                          dense
                        />
                      </div>
                      <div class="q-mt-lg">
                        <q-input
                          v-model="form.claim_description"
                          label="Claim description"
                          dark
                          label-color="white"
                          color="white"
                          dense
                          type="textarea"
                          autogrow
                        />
                      </div>
                      <div class="q-mt-lg">
                        <q-file
                          color="white"
                          v-model="form.claim_file"
                          label="Claim file"
                          label-color="white"
                          dense
                          dark
                        >
                          <template v-slot:prepend>
                            <q-icon color="white" name="attach_file" />
                          </template>
                        </q-file>
                      </div>
                      <div class="q-mt-lg">
                        <q-input
                          v-model="form.claim_amount"
                          label="Amount"
                          dark
                          label-color="white"
                          color="white"
                          dense
                          type="number"
                        />
                      </div>
                      <div class="q-mt-lg">
                        <q-input
                          v-model="form.remarks"
                          label="Remarks"
                          dark
                          label-color="white"
                          color="white"
                          dense
                          type="textarea"
                          autogrow
                        />
                      </div>
                      <div class="q-mt-lg q-mb-lg flex flex-center">
                        <q-btn
                          class="submit-btn"
                          outline
                          color="white"
                          label="Submit Claim"
                        />
                      </div>
                    </div>
                  </div>
                </div>
              </q-tab-panel>
            </q-tab-panels>
          </div>
        </div>
      </div>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";
import ProductSold from "../components/Charts/ProductSold.vue";
import TopSoldProduct from "../components/Charts/TopSoldProduct.vue";
import CashCollection from "../components/Charts/CashCollection.vue";
import SalesAndReceivable from "../components/Charts/SalesAndReceivable.vue";
import SrSales from "../components/Charts/SrSales.vue";
import TopDistrict from "../components/Charts/TopDistrict.vue";
import NewPurchased from "../components/Charts/NewPurchased.vue";
import AvailableProducts from "../components/Charts/AvailableProducts.vue";
import AxePrice from "../components/Charts/AxePrice.vue";
import DovePrice from "../components/Charts/DovePrice.vue";
import PersilPrice from "../components/Charts/PersilPrice.vue";
import ComfortPrice from "../components/Charts/ComfortPrice.vue";
import SimplePrice from "../components/Charts/SimplePrice.vue";
import TresemmePrice from "../components/Charts/TresemmePrice.vue";
import CamayPrice from "../components/Charts/CamayPrice.vue";
import BruPrice from "../components/Charts/BruPrice.vue";
import PearsPrice from "../components/Charts/PearsPrice.vue";
export default defineComponent({
  name: "IndexPage",
  components: {
    ProductSold,
    TopSoldProduct,
    CashCollection,
    SalesAndReceivable,
    SrSales,
    TopDistrict,
    NewPurchased,
    AvailableProducts,
    AxePrice,
    DovePrice,
    PersilPrice,
    ComfortPrice,
    SimplePrice,
    TresemmePrice,
    CamayPrice,
    BruPrice,
    PearsPrice,
  },
  data() {
    return {
      tab: "MY_KPIs",
      tab2: "Axe",
      form: {
        claim_title: "",
        claim_description: "",
        claim_file: "",
        claim_amount: "",
        remarks: "",
      },
    };
  },
});
</script>

<style lang="scss" scoped>
.head {
  color: #102a43;
}

.bg {
  background-color: #f1f5f8;
  width: 100%;
  min-height: 90vh;
}

.tab-bg {
  background-color: #f1f5f8;
}

.srs {
  height: 350px;
  color: #102a43;
  font-size: 14px;
}

.poa {
  height: 350px;
  color: #102a43;
  font-size: 14px;
}

.cc {
  height: 350px;
  color: #102a43;
  font-size: 14px;
}

.shop_sr {
  height: 350px;
}

.tsp {
  height: 350px;
  color: #102a43;
  font-size: 14px;
}

.bdmap {
  height: 350px;
  color: #102a43;
  font-size: 14px;
}

.map {
  height: 350px;
}

.top_district {
  height: 350px;
  color: #102a43;
  font-size: 14px;
}

.tso {
  height: 510px;
  color: #102a43;
  font-size: 14px;
}

.tms {
  height: 200px;
}

.bap {
  height: 350px;
  color: #102a43;
  font-size: 14px;
}

.npi {
  height: 380px;
  color: #102a43;
  font-size: 14px;
}

.pp {
  height: 380px;
  color: #102a43;
  font-size: 14px;
}

.q-tab-panel {
  padding: 0px;
}

.form {
  background: linear-gradient(to right, #9d3c86, #631ca2);
}
.submit-btn:hover {
  color: #9d3c86 !important;
  background: white !important;
}
</style>

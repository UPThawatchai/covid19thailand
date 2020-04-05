<template style="color:white" id="temp">
  <div class="content">
    <div class="row">
      <div class="col-12">
        <card type="chart">
          <template slot="header">
            <div class="row">
              <div class="col-sm-12 text-left">
                <template>
                  <label
                    style="font-size:20px;color: #f7f7f7;"
                    class="card-category"
                  >ไวรัสโคโรน่าสายพันธุ์ใหม่ 2019 (Novel Coronavirus 2019) อัพเดทล่าสุดวันที่ {{ title }}</label>
                </template>
              </div>
            </div>
          </template>
          <canvas id="thai-covid19-chart" width="500" height="90"></canvas>
        </card>
      </div>
    </div>
    <!-- <div class="col-lg-6 col-md-6">
      <div class="card card-stats">
        <div class="card-body">
          <div class="row">
            <div class="col-5">
              <div class="info-icon text-center icon-info">
                <i style="font-size: 2.0625rem" class="tim-icons icon-credit-card"></i>
              </div>
            </div>
            <div class="col-6">
              <div class="numbers">
                <p class="card-category">รายชื่อประเทศที่ติดเชื้อ</p>
              </div>
            </div>
          </div>
          <card style="margin-bottom:unset;height: 105px;" type="tasks">
            <div class="table-full-width table-responsive">
              <div class="countries-list">
                <tr v-for="row in countries" :key="row.index">
                  <td>
                    <p style="font-size:1.0625rem" class="text-muted">{{ row.TotalConfirmed }}</p>
                  </td>
                  <td class="text-left">
                    <p style="font-size:1.0625rem" class="card-title">{{ row.Country }}</p>
                  </td>
                </tr>
              </div>
            </div>
          </card>
        </div>
        <div class="card-footer">
          <hr />
          <div class="stats">
            <div>เวลาโลก : {{ allDate }}</div>
          </div>
        </div>
      </div>
    </div>-->
    <!-- <div class="col-lg-3 col-md-6">
      <div class="card card-stats">
        <div class="card-body">
          <div class="row" style="margin-bottom: 13px;">
            <div class="col-5">
              <div class="info-icon text-center icon-info">
                <i style="font-size: 2.0625rem" class="tim-icons icon-trophy"></i>
              </div>
            </div>
            <div class="col-6">
              <div class="numbers">
                <p class="card-category">อับดับติดเชื้อไวรัสสูงที่สุด</p>
              </div>
            </div>
          </div>
          <div class="row" style="margin: 10px;">
            <div class="col-7">
              <h4 class="card-title">{{ winName2 }}</h4>
            </div>
            <div class="col-5">
              <h4 class="card-title">{{ winConfirmed2 }}</h4>
            </div>
          </div>
          <div class="row" style="margin: 10px;">
            <div class="col-7">
              <h4 class="card-title">{{ winName1 }}</h4>
            </div>
            <div class="col-5">
              <h4 class="card-title">{{ winConfirmed1 }}</h4>
            </div>
          </div>
        </div>
        <div class="card-footer">
          <hr />
          <div class="stats">
            <div>เวลาโลก : {{ allDate }}</div>
          </div>
        </div>
      </div>
    </div>-->
    <div class="col-lg-3 col-md-6">
      <div class="card card-stats">
        <div class="card-body" style="height: 178px;">
          <div class="row">
            <div class="col-5">
              <div class="info-icon text-center icon-info">
                <i style="font-size: 2.0625rem" class="tim-icons icon-square-pin"></i>
              </div>
            </div>
            <div class="col-7" id="istemp">
              <div class="numbers" id="istesmp">
                <p class="card-category">ติดเชื้อไวรัสในไทย</p>
                <h3 class="card-title">{{ thAll }}</h3>
              </div>
            </div>
            <div class="col-6">
              <div class="numbers">
                <p class="card-category">ตาย</p>
                <h3 class="card-title">{{ thDeads }}</h3>
              </div>
            </div>
            <div class="col-6">
              <div class="numbers">
                <p class="card-category">รักษาหาย</p>
                <h3 class="card-title">{{ thRecovery }}</h3>
              </div>
            </div>
          </div>
        </div>
        <div class="card-footer">
          <hr />
          <div class="stats">
            <div>เวลาในไทย : {{ thDate }}</div>
          </div>
        </div>
      </div>
    </div>
    <div class="col-lg-3 col-md-6">
      <div class="card card-stats">
        <!---->
        <div class="card-body" style="height: 178px;">
          <div class="row">
            <div class="col-5">
              <div class="info-icon text-center icon-danger">
                <i style="font-size: 2.0625rem" class="tim-icons icon-planet"></i>
              </div>
            </div>
            <div class="col-7">
              <div class="numbers">
                <p class="card-category">ผู้ติดเชื้อไวรัสทั่วโลก</p>
                <h3 class="card-title">{{ allData }}</h3>
              </div>
            </div>
            <div class="col-6">
              <div class="numbers">
                <p class="card-category">ตาย</p>
                <h3 class="card-title">{{ allDeads }}</h3>
              </div>
            </div>
            <div class="col-6">
              <div class="numbers">
                <p class="card-category">รักษาหาย</p>
                <h3 class="card-title">{{ allRecovery }}</h3>
              </div>
            </div>
          </div>
        </div>
        <!---->
        <div class="card-footer">
          <hr />
          <div class="stats">
            <div>
              <!-- <i class="tim-icons icon-watch-time"></i> -->
              เวลาโลก : {{ hours }}
              <!-- อัพเดทเวลา {{ hours }} -->
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="col-lg-6 col-md-6">
      <div class="card card-stats">
        <!---->
        <div class="card-body">
          <div class="row">
            <div class="col-2">
              <div class="numbers">
                <p class="card-category">รักษาหาย</p>
              </div>
            </div>
            <div class="col-2">
              <div class="numbers">
                <p class="card-category">ติดเชื้อทั้งหมด</p>
              </div>
            </div>
            <div class="col-2">
              <div class="numbers">
                <p class="card-category">ตายสะสม</p>
              </div>
            </div>
            <div class="col-6">
              <div class="numbers" style="text-align: left;margin-left: 30px;">
                <p class="card-category">รายชื่อประเทศที่ติดเชื้อ</p>
              </div>
            </div>
            <div class="col-12">
              <div
                style="margin-bottom:unset;height: 115px;"
                class="table-full-width table-responsive"
              >
                <tr v-for="row in countries" :key="row.index">
                  <td class="text-center">
                    <p
                      style="font-size: 1.0625rem;width: 85px;"
                      class="text-muted"
                    >{{ row.TotalRecovered }}</p>
                  </td>
                  <td class="text-center">
                    <p
                      style="font-size:1.0625rem;width: 135px;"
                      class="card-title"
                    >{{ row.TotalConfirmed }}</p>
                  </td>
                  <td class="text-center">
                    <p
                      style="font-size:1.0625rem;width: 90px;"
                      class="card-title"
                    >{{ row.TotalDeaths }}</p>
                  </td>
                  <td class="text-left">
                    <p
                      style="font-size:1.0625rem;width: 290px;"
                      class="card-title"
                    >{{ row.Country }}</p>
                  </td>
                </tr>
              </div>
            </div>
          </div>
        </div>
        <!---->
        <div class="card-footer">
          <hr />
          <div class="stats">
            <div>
              <!-- <i class="tim-icons icon-watch-time"></i> -->
              เวลาโลก : {{ hours }}
              <!-- อัพเดทเวลา {{ hours }} -->
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import Vue from "vue";
import { Card } from "@/components/index";
import { MdContent } from "vue-material/dist/components";
import "vue-material/dist/vue-material.min.css";

Vue.config.productionTip = false;
import axios from "axios";
import moment from "moment";
import * as chartConfigs from "@/components/Charts/config";
import config from "@/config";
import Chart from "chart.js";
Vue.use(MdContent);

export default {
  name: "countries-list",
  components: {
    Card
    // LineChart
  },
  data() {
    return {
      title: "",
      hours: "",
      allData: "",
      allRecovery: "",
      allDeads: "",
      //-----------
      thAll: "",
      thRecovery: "",
      thDeads: "",
      th: "",
      thDate: "",
      //----------
      winName1: "",
      winConfirmed1: "",
      winName2: "",
      winConfirmed2: "",
      countries: [],
      allDate: "",
      // covid19Start: [],
      // covid19Confirmed: [],
      // covid19Recovered: [],
      // covid19Deaths: []
      provinces: [],
      totalsConfirm: []
    };
  },
  methods: {
    titleChart(title) {
      return moment(String(title)).format("DD/MMM/YYYY HH:mm:ss");
    },
    timeHours(time) {
      return moment(String(time)).format("DD MM HH:mm");
    },
    thDateTime(time) {
      return moment(String(time)).format("DD MMM HH:mm");
    },
    covid19StartDate(time) {
      return moment(String(time)).format("DD MMM");
    },
    // sortAppointments(param) {
    //   return param.sort((a, b) => a.TotalConfirmed - b.TotalConfirmed);
    // },
    subStrCountries(country) {
      return country == "United States of America" ? "United States" : country;
    }
  },
  mounted() {
    //GET CHART START===============
    axios
      .get("https://covid19.th-stat.com/api/open/cases/sum")
      .then(response => {
        if (null != response && response.status == 200) {
          // debugger;
          console.log(response);
          let pro = [];
          let totals = [];
          // console.log(Object.entries(response.data.Province));
          Object.entries(response.data.Province).forEach(map => {
            pro.push(map[0]);
            totals.push(map[1]);
          });
          this.provinces = pro;
          this.totalsConfirm = totals;
          new Chart(document.getElementById("thai-covid19-chart"), {
            type: "line",
            data: {
              labels: this.provinces,
              datasets: [
                {
                  label: "จังหวัด",
                  data: this.totalsConfirm,
                  borderColor: "rgba(255, 56, 96, 0.5)",
                  backgroundColor: "rgba(255, 56, 96, 0.1)"
                }
              ]
            }
          });
        }
      });
    //GET CHART END===============
    //GET TOTAL START===============
    var config = {
      headers: {
        "x-rapidapi-host": "coronavirus-monitor.p.rapidapi.com",
        "x-rapidapi-key": "5156f83861mshd5c5731412d4c5fp18132ejsn8ae65e661a54",
        crossDomain: true
      }
    };
    axios
      .get(
        "https://coronavirus-monitor.p.rapidapi.com/coronavirus/worldstat.php",
        config
      )
      .then(response => {
        if (null != response && response.status == 200) {
          this.title = this.titleChart(response.data.statistic_taken_at);
          this.allData = response.data.total_cases;
          this.hours = this.thDateTime(response.data.statistic_taken_at);
          this.allRecovery = response.data.total_recovered;
          this.allDeads = response.data.total_deaths;
        }
      })
      .catch(error => {
        console.log(error);
        console.log("Not good man :(");
      });

    //GET TOTAL END===============
    //GET Thailand START===============
    axios
      .get("https://covid19.th-stat.com/api/open/today")
      .then(response => {
        if (null != response && response.status == 200) {
          this.thAll = response.data.Confirmed;
          this.thDeads = response.data.Deaths;
          this.thRecovery = response.data.Recovered;
          this.thDate = this.thDateTime(response.data.UpdateDate);
        }
      })
      .catch(error => {
        console.log(error);
        console.log("Not good man :(");
      });

    //GET Thailand END===============
    //GET TOP AND ALL START===============
    axios
      .get("https://api.covid19api.com/summary")
      .then(response => {
        if (null != response && response.status == 200) {
          let allContries = [];
          let index = 0;
          //Find all
          let sortData = response.data.Countries;
          sortData.forEach(element => {
            if ("" != element.Country && element.TotalConfirmed > 0) {
              element.index = index++;
              allContries.push(element);
            }
          });
          this.countries = allContries;
          //Find top
          // let countryUs1 = this.subStrCountries(
          //   sortData[sortData.length - 2].Country
          // );
          // let countryUs2 = this.subStrCountries(
          //   sortData[sortData.length - 1].Country
          // );
          // this.winName2 = countryUs2;
          // this.winConfirmed2 = sortData[sortData.length - 1].TotalConfirmed;
          // this.winName1 = countryUs1;
          // this.winConfirmed1 = sortData[sortData.length - 2].TotalConfirmed;
          // this.allDate = this.thDateTime(response.data.Date);
        }
      })
      .catch(error => {
        console.log("Not good man :(");
        console.log(error);
      });
    //GET TOP AND ALL END===============
  }
};
</script>

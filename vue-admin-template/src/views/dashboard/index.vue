<template>
  <div class="dashboard-container">
    <panel-group/>
    <el-row class="graph-container" :style="{height:rankHeight}" style="padding: 16px 16px;">
      <TotalRank ref="totalRank"></TotalRank>
    </el-row>
    <el-row>
      <el-col :span="11" class="graph-container" :style="{height:secondHeight}">
        <LanguageRanks ref="rank" :hgt="rankhgt"></LanguageRanks>
      </el-col>
      <el-col :span="1" style="border: 1px solid transparent">
      </el-col>
      <el-col :span="12" class="graph-container" :style="{height:secondHeight}">
        <NumberRatioByTime></NumberRatioByTime>
      </el-col>
    </el-row>
  </div>
</template>

<script>
import {mapGetters} from 'vuex'
import LanguageRanks from "@/views/dashboard/components/LanguageRanks";
import RelationshipJava from "@/views/form/components/RelationshipJava";
import PanelGroup from "@/views/dashboard/components/PanelGroup";
import TotalRank from "@/views/dashboard/components/TotalRank";
import NumberRatioByTime from "@/views/dashboard/components/NumberRatioByTime";
import axios from "axios";

export default {
  name: 'Dashboard',
  data() {
    return {}
  },
  computed: {
    ...mapGetters([
      'name'
    ]),
    rankHeight() {
      return window.innerHeight * 0.4 + "px";
    },
    secondHeight() {
      return window.innerHeight * 0.5 + "px";
    },
    rankhgt() {
      return window.innerHeight * 0.45 + "px";
    }
  },
  components: {
    NumberRatioByTime,
    TotalRank,
    RelationshipJava,
    LanguageRanks,
    PanelGroup
  },
  mounted() {
  },
  watch: {}
}
</script>

<style lang="scss" scoped>
.dashboard {
  &-container {
    margin: 30px;
  }

  &-text {
    font-size: 30px;
    line-height: 46px;
  }
}

.dashboard-container {
  padding: 32px;
  background-color: rgb(240, 242, 245);
  position: relative;

}

.graph-container {
  background: #fff;
  padding: 16px 16px;
  margin-bottom: 32px;
}
</style>

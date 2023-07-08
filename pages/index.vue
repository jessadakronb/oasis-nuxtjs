<template>
  <div>
    <!-- <h1 class="text-2xl font-bold">Dashboard</h1> -->
    <div class="dashboard-grid">
      <div class="dashboard-card bg-custom-purple">
        <h2 class="text-lg font-semibold text-white">วันลาที่เหลือทั้งหมด</h2>
        <p class="text-xl text-white">{{ totalLeaveDays }}</p>
      </div>
      <div class="dashboard-card bg-custom-blue">
        <h2 class="text-lg font-semibold text-white">วันลากิจ</h2>
        <p class="text-xl text-white">{{ personalLeaveDays }}</p>
      </div>
      <div class="dashboard-card bg-custom-yellow">
        <h2 class="text-lg font-semibold text-white">วันลาป่วย</h2>
        <p class="text-xl text-white">{{ sickLeaveDays }}</p>
      </div>
      <div class="dashboard-card bg-custom-red">
        <h2 class="text-lg font-semibold text-white">วันลาพักร้อน</h2>
        <p class="text-xl text-white">{{ vacationLeaveDays }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  layout: 'default',
  data() {
    return {
      totalLeaveDays: 10, // จำนวนวันลาที่เหลือทั้งหมด
      personalLeaveDays: 3, // จำนวนวันลากิจ
      sickLeaveDays: 4, // จำนวนวันลาป่วย
      vacationLeaveDays: 2, // จำนวนวันลาพักร้อน
      otherLeaveDays: 1, // จำนวนวันลาอื่นๆ
    };
  },
};
</script>

<style scoped>
.dashboard-grid {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  margin-top: 20px;
}

@media (max-width: 767px) {
  .dashboard-grid {
    justify-content: center;
  }
}

.dashboard-card {
  padding: 1rem;
  width: 230px;
  margin-bottom: 1rem;
  margin-left: 1rem;
  margin-right: 1rem;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.bg-custom-purple {
  background-color: #321FDA;
}

.bg-custom-blue {
  background-color: #3399FE;
}

.bg-custom-yellow {
  background-color: #F8B114;
}

.bg-custom-red {
  background-color: #E55352;
}
</style>

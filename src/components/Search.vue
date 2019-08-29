<template>
        <section class="search">
        <div class="search-wrap">
          <div class="search-icon">
            <svg
              version="1.1"
              id="search-svg"
              xmlns="http://www.w3.org/2000/svg"
              xmlns:xlink="http://www.w3.org/1999/xlink"
              x="0px"
              y="0px"
              viewBox="0 0 96 96"
              xml:space="preserve"
            >
              <g id="XMLID_2_">
                <path
                  id="XMLID_6_"
                  class="st0"
                  d="M58.6,43.8c0-4.1-1.4-7.6-4.3-10.5c-2.9-2.9-6.4-4.3-10.5-4.3s-7.6,1.4-10.5,4.3
                           c-2.9,2.9-4.3,6.4-4.3,10.5s1.4,7.6,4.3,10.5c2.9,2.9,6.4,4.3,10.5,4.3s7.6-1.4,10.5-4.3C57.1,51.3,58.6,47.8,58.6,43.8z
                            M75.5,71.3c0,1.1-0.4,2.1-1.3,3s-1.8,1.3-3,1.3c-1.2,0-2.2-0.4-3-1.3L57,62.9C53,65.7,48.6,67,43.8,67c-3.2,0-6.2-0.6-9-1.8
                           c-2.9-1.2-5.4-2.9-7.4-5s-3.7-4.6-5-7.4c-1.2-2.9-1.8-5.9-1.8-9s0.6-6.2,1.8-9c1.2-2.9,2.9-5.4,5-7.4s4.6-3.7,7.4-5
                           c2.9-1.2,5.9-1.8,9-1.8s6.2,0.6,9,1.8c2.9,1.2,5.4,2.9,7.4,5s3.7,4.6,5,7.4c1.2,2.9,1.8,5.9,1.8,9c0,4.8-1.4,9.2-4.1,13.2
                           l11.3,11.3C75.1,69.1,75.5,70.1,75.5,71.3z"
                />
              </g>
            </svg>
          </div>
          <input type="text" placeholder="Product Model / Keywords e.g." v-model="keyWord"/>
        </div>
      </section>
</template>

<script>
export default {
    name: 'Search',
    data() {
        return {}
    },
    props: ["keyWord"]
}
</script>

<style>
.search {
    padding: 70px 0;
}
.search-wrap {
    display: flex;
    height: 80px;
    width: 100%;
    border: 1px solid #c0c0c0;
    border-radius: 2px;
}

.search-icon, #search-svg {
    height: inherit;
}

#search-svg {
    fill: #575756;
}

.search-wrap > input {
    border: none;
    width: 100%;
    font-size: 26px;
    color: #bab1af;
    font-weight: bold;
    outline: none;
    padding-left: 20px;
}

.search-wrap > input::placeholder {
    color: #bab1af;
}
</style>
<template>
    <div class="wrapper">
        <div class="header">
            <div class="name">
                <h1>Björn Andersson</h1>
            </div>
            <nav>
                <div class="link">
                    <div class="b">
                        <router-link to="/">Home</router-link>
                    </div>
                </div>
                <div class="boop">
                        <b-dropdown id="dropdown-1" text="Week" class="m-md-2">
                            <router-link class="full" to="/week">
                                <b-dropdown-item>
                                    Week1
                                </b-dropdown-item>
                            </router-link>
                            <b-dropdown-item>
                                <router-link class="full" to="/week2">Week2</router-link>
                            </b-dropdown-item>
                        </b-dropdown>
                </div>
            </nav>
        </div>
        <div class="content">
            <div class="text">
                <h1>About me</h1>
                <p>
                    Hello im a 22 year old webdeveloping student interested in frontend design and development. I'm from a small town in northern Småland known for swedish style cheesecake and Astrid Lindgren.
                    I play tennis, golf and videogames on my freetime and love to cook as well when i get the opurtunity.
                    <br>
                    I look forward to learning more about js frameworks since ive worked with them before but never vue and never truely indepth so i think this will be facinating.
                </p>
            </div>
            <div class="img">
                <img src="../assets/Me.jpg" alt="hej">
            </div>
        </div>
        <h1 class="title">Registration form</h1>
        <div class="form">
          <b-form @submit="onSubmit" @reset="onReset" v-if="show">
            <b-form-group
              id="input-group-1"
              label="Email address:"
              label-for="input-1"
              description="We'll never share your email with anyone else."
            >
              <b-form-input
                id="input-1"
                v-model="form.email"
                type="email"
                required
                pattern="[a-z0-9._%+-]+@[a-z0-9.-]+\.[a-z]{2,}$"
              ></b-form-input>
            </b-form-group>

            <b-form-group id="input-group-2" label="Your name:" label-for="input-2">
              <b-form-input
                id="input-2"
                v-model="form.name"
                required
                pattern="[^<>/]+"
              ></b-form-input>
            </b-form-group>

            <b-form-group id="input-group-3" label="Your password:" label-for="input-3" description="Please use at least one capital letter one small letter and a number">

              <b-form-input
                id="input-3"
                v-model="form.password"
                type="password"
                required
                pattern="(?=.*\d)(?=.*[a-z])(?=.*[A-Z]).{8,}"
              ></b-form-input>
            </b-form-group>

            <b-form-group id="input-group-4" label="Your birthday:" label-for="input-4">
                <div class="input">
                    <div class="input-box">
                        <p>Year</p>
                        <b-form-input
                            list="my-list-id-1"
                            v-model="form.year"
                            required
                            pattern="(?:19|20)\d\d"
                        ></b-form-input>
                    </div>
                    <br>
                    <div class="input-box">
                        <p>Month</p>
                        <b-form-input
                            list="my-list-id-2"
                            v-model="form.month"
                            required
                        ></b-form-input>
                    </div>
                    <br>
                    <div class="input-box">
                        <p>Day</p>
                        <b-form-input
                            list="my-list-id-3"
                            v-model="form.day"
                            required
                            pattern="^(3[01]|[12][0-9]|[1-9])$"
                        ></b-form-input>
                    </div>
                </div>

                <datalist id="my-list-id-1">
                      <option>Manual Option</option>
                      <option v-for="num in 100" :key="num">{{ num + 1909 }}</option>
                </datalist>
                <datalist id="my-list-id-2">
                      <option>Manual Option</option>
                      <option v-for="month in 12" :key="month">{{ month }}</option>
                </datalist>
                <datalist id="my-list-id-3">
                      <option>Manual Option</option>
                      <option v-for="day in 31" :key="day">{{ day }}</option>
                </datalist>

              <!-- <b-form-input
                id="input-4"
                v-model="form.date"
                type="date"
                pattern="([12]\d{3}-(0[1-9]|1[0-2])-(0[1-9]|[12]\d|3[01]))"
                required
              ></b-form-input> -->
            </b-form-group>

            <b-form-group id="input-group-5">
              <b-form-checkbox-group v-model="form.checked" required id="checkboxes-5">
                <b-form-checkbox value="x">Agree to terms</b-form-checkbox>
              </b-form-checkbox-group>
            </b-form-group>

            <b-button type="submit" variant="primary">Submit</b-button>
            <b-button type="reset" variant="danger">Reset</b-button>
          </b-form>
          <b-card class="mt-3" header="Form Data Result">
            <pre class="m-0">{{ form }}</pre>
          </b-card>
        </div>
    </div>
</template>

<script>


export default {
      data() {
        return {
          form: {
            email: '',
            name: '',
            password: '',
            food: null,
            year: '',
            month: '',
            day: '',
            checked: []
          },
          show: true
        }
      },
      methods: {
        onSubmit(evt) {
          evt.preventDefault()
          alert(JSON.stringify(this.form))
        },
        onReset(evt) {
          evt.preventDefault()
          // Reset our form values
          this.form.email = ''
          this.form.name = ''
          this.form.name = ''
          this.form.years = ''
          this.form.password = ''
          this.form.food = null
          this.form.checked = []
          // Trick to reset/clear native browser form validation state
          this.show = false
          this.$nextTick(() => {
            this.show = true
          })
        }
      }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
    .wrapper .content {
        display: flex;
        margin-top: 100px;
    }
    .wrapper .content .text {
        margin-left: 8%;
        padding-left: 2%;
        margin-right: 10%;
        width: 30%;
        border-left: 2px solid #8CB5CA;
        border-right: 2px solid #8CB5CA;
    }

    .wrapper .content .text p {
        margin-top: 70px;
    }

    .wrapper .content .img img {
        width: 500px;
    }

    .form {
        display: flex;
        justify-content: center;
        margin-top: 50px;
        margin-bottom: 100px;
    }
    form {
        width: 50%;
    }
    .card {
        width: 300px;
    }
    #input-group-1 {
        width: 50%;
    }
    #input-group-2 {
        width: 50%;
    }
    #input-group-3 {
        width: 50%;
    }
    #input-group-4 {
        width: 50%;
        border: 0;
        font-family: Montserrat;
    }
    .input {
        display: flex;
        flex-direction: row;
    }
    .input-box {
        text-align: center;
    }
    .input-box p {
        margin-bottom: 0;
    }
    .title {
        width: 100%;
        text-align: center;
        margin-top: 100px;
    }
</style>

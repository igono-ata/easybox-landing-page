<template>
  <div>
    <div
      class="container-fluid"
      style="background-image: url('/store-owner.jpg'); background-size: cover"
    >
      <div class="row" style="height: 91vh">
        <div class="container-lg"></div>
        <div class="col-lg-4 offset-lg-2" style="text-align: left">
          <div class="">
            <h1 style="color: #fff">
              <strong
                >Become a
                <span style="color: #73dbac">Digital Finance Associate</span>
              </strong>
            </h1>
            <h4 style="color: #fff">You'll get:</h4>
            <h4 style="color: #fff">
              Certification | Work Experience | Mentorship
            </h4>
            <br />
            <b-button
              pill
              v-b-modal.modal-1
              style="background: #73dbac; color: #34495e; border: none"
            >
              <strong style="color: #000">Start Now</strong>
            </b-button>
            &nbsp;
            <b-button
              pill
              style="background: white; color: #34495e; border: none"
              href="#about"
              ><strong>Find out more</strong></b-button
            >
            <b-modal
              size="lg"
              ref="modal-1"
              id="modal-1"
              title="Become a Digital Finance Associate"
              :hideFooter="true"
            >
              <div class="container">
                <form inline>
                  <div class="row">
                    <div class="col-lg-6">
                      <label class="sr-only" for="inline-form-input-firstname"
                        >First Name</label
                      >
                      <br />
                      <input
                        id="inline-form-input-name"
                        class="mb-2 mr-sm-2 mb-sm-0"
                        placeholder=""
                        required
                        type="text"
                        v-model="firstname"
                      />
                    </div>
                    <div class="col-lg-6">
                      <label class="sr-only" for="inline-form-input-lastname"
                        >Last Name</label
                      >
                      <br />
                      <input
                        id="inline-form-input-username"
                        placeholder=""
                        required
                        type="text"
                        v-model="lastname"
                      />
                    </div>
                  </div>
                  <br />
                  <div class="row">
                    <div class="col-lg-6">
                      <label class="sr-only" for="inline-form-input-phone"
                        >Phone Number</label
                      >
                      <br />
                      <input
                        id="inline-form-input-name"
                        class="mb-2 mr-sm-2 mb-sm-0"
                        placeholder=""
                        type="phone"
                        required
                        v-model="phone"
                      />
                    </div>
                    <div class="col-lg-6">
                      <label class="sr-only" for="inline-form-input-email"
                        >Email</label
                      >
                      <br />
                      <input
                        id="inline-form-input-username"
                        placeholder=""
                        type="email"
                        required
                        v-model="email"
                      />
                    </div>
                  </div>
                  <br />
                  <div class="row">
                    <div class="col-lg-6">
                      <label class="sr-only" for="inline-form-gender"
                        >Gender</label
                      >
                      <br />
                      <b-form-select
                        v-model="gender"
                        required
                        :options="genderOptions"
                      ></b-form-select>
                    </div>
                    <div class="col-lg-6">
                      <label class="sr-only" for="inline-form-gender"
                        >State</label
                      >
                      <br />
                      <b-form-select
                        v-model="state"
                        required
                        :options="stateOptions"
                      ></b-form-select>
                    </div>
                  </div>
                  <br />
                  <div class="row">
                    <div class="col-lg-6">
                      <label class="sr-only" for="inline-form-work"
                        >Work Experience</label
                      >
                      <br />
                      <b-form-select
                        v-model="work"
                        required
                        :options="workOptions"
                      ></b-form-select>
                    </div>
                    <div class="col-lg-6">
                      <label class="sr-only" for="inline-form-edu"
                        >Education</label
                      >
                      <br />
                      <b-form-select
                        v-model="education"
                        required
                        :options="eduOptions"
                      ></b-form-select>
                    </div>
                  </div>
                  <br />
                  <div class="row">
                    <div class="col-lg-6">
                      <label class="sr-only" for="inline-form-input-dob"
                        >Date of Birth</label
                      >
                      <b-form-datepicker
                        id="date"
                        required
                        v-model="dob"
                        class="mb-2"
                      ></b-form-datepicker>
                    </div>
                  </div>
                  <br />
                  <div class="row">
                    <div class="col-lg-10">
                      <label class="sr-only" for="inline-form-input-what"
                        >What is your current address?</label
                      >
                      <br />
                      <b-form-textarea
                        id="address"
                        v-model="address"
                        required
                        placeholder="Enter something..."
                        rows="3"
                        max-rows="6"
                      ></b-form-textarea>
                    </div>
                  </div>
                  <br />
                  <div class="row">
                    <div class="col-lg-12">
                      <label class="sr-only" for="inline-form-work"
                        >Are you willing to commit the next 2-3 months to
                        digital selling and SME support activities?</label
                      >
                      <br />
                      <b-form-select
                        v-model="commit"
                        required
                        :options="commitOptions"
                      ></b-form-select>
                    </div>
                  </div>
                </form>
                <br />
                <b-button
                  v-b-modal.modal-2
                  @click="hide1()"
                  pill
                  style="background: #73dbac; color: #000; border: none"
                  >Next</b-button
                >
                1/3
              </div>
            </b-modal>
            <b-modal
              size="lg"
              ref="modal-2"
              id="modal-2"
              title="Become a Digital Finance Associate"
              :hideFooter="true"
            >
              <div class="container">
                <form inline>
                  <div class="row">
                    <div class="col-lg-12">
                      <label class="sr-only" for="inline-form-input-devices"
                        >Which of the following devices do you have access
                        to?</label
                      >
                      <br />
                      <b-form-group>
                        <b-form-checkbox-group
                          id="checkbox-group-2"
                          v-model="devices"
                          inline
                          required
                        >
                          <b-form-checkbox value="smartphone"
                            >&nbsp;Smart phone</b-form-checkbox
                          >
                          <b-form-checkbox value="tablet"
                            >&nbsp;Tablet</b-form-checkbox
                          >
                          <b-form-checkbox value="laptop"
                            >&nbsp;Laptop</b-form-checkbox
                          >
                          <b-form-checkbox value="desktop"
                            >&nbsp;Desktop</b-form-checkbox
                          >
                        </b-form-checkbox-group>
                      </b-form-group>
                    </div>
                  </div>
                  <hr />
                  <div class="row">
                    <div class="col-lg-12">
                      <label class="sr-only" for="inline-form-input-access"
                        >On the average, how many hours of access do you have to
                        the internet and electricity daily?</label
                      >
                      <br />
                      <b-form-select
                        v-model="access"
                        required
                        :options="accessOptions"
                      ></b-form-select>
                    </div>
                  </div>
                  <br />
                  <div class="row">
                    <div class="col-lg-12">
                      <label class="sr-only" for="business"
                        >Do you have a current business?
                      </label>
                      <br />
                      <b-form-select
                        v-model="business"
                        required
                        :options="businessOptions"
                      ></b-form-select>
                    </div>
                  </div>
                  <br />
                  <div class="row">
                    <label for="bizType">If yes, what type of business?</label>
                    <br />
                    <b-form-input
                      id="input-default"
                      v-model="bizType"
                      placeholder="Busines type"
                    ></b-form-input>
                  </div>
                  <br />
                  <div class="row">
                    <label for="income"
                      >On an average, what's your income from their current
                      business?</label
                    >
                    <b-form-input
                      id="input-default"
                      v-model="income"
                      placeholder="Naira amount"
                    ></b-form-input>
                  </div>
                  <br />
                  <div class="row">
                    <div class="col-lg-12">
                      <label class="sr-only" for="business"
                        >Do you have a physical business location?
                      </label>
                      <br />
                      <b-form-select
                        v-model="location"
                        required
                        :options="locationOptions"
                      ></b-form-select>
                    </div>
                  </div>
                  <br />
                  <b-button
                    @click="hide2()"
                    v-b-modal.modal-3
                    pill
                    style="background: #73dbac; color: #000; border: none"
                    >Next</b-button
                  >
                  2/3
                </form>
              </div>
            </b-modal>
            <b-modal
              size="lg"
              ref="modal-3"
              id="modal-3"
              title="Become a Digital Finance Associate"
              :hideFooter="true"
            >
              <div class="container">
                <form inline>
                  <div class="row">
                    <div class="col-lg-10">
                      <label class="sr-only" for="inline-form-input-why"
                        >Why do you want to be an SME Digital Finance Associate?
                        (100 words max)</label
                      >
                      <br />
                      <b-form-textarea
                        id="why"
                        v-model="why"
                        required
                        placeholder="Enter something..."
                        rows="3"
                        max-rows="6"
                      ></b-form-textarea>
                    </div>
                  </div>
                  <br />
                  <div class="row">
                    <div class="col-lg-12">
                      <b-form-group
                        label="How did you hear about the SME Digital finance associate program?"
                      >
                        <b-form-checkbox-group
                          id="checkbox-group-2"
                          v-model="hear"
                        >
                          <b-form-checkbox value="Friend, colleague or network"
                            >&nbsp;Friend, colleague or network</b-form-checkbox
                          >
                          <b-form-checkbox value="Social media"
                            >&nbsp;Social media</b-form-checkbox
                          >
                          <b-form-checkbox value="Google"
                            >&nbsp;Google</b-form-checkbox
                          >
                          <b-form-checkbox value="Easy finance partner"
                            >&nbsp;EasyBox partner</b-form-checkbox
                          >
                        </b-form-checkbox-group>
                      </b-form-group>
                      <br />
                    </div>
                  </div>
                  <div class="row">
                    <b-form-group label="Upload a Photo ID">
                      <b-form-file
                        id="photo"
                        @change="imageToURL()"
                        accept="image/jpeg, image/png, image/gif"
                      ></b-form-file>
                    </b-form-group>
                  </div>
                  <p v-if="size_error" class="alert-danger">{{ size_error }}</p>
                  <hr />
                </form>
              </div>
              <footer>
                After you submit your survey you'll be contacted to create an
                account.
              </footer>
              <hr />
              <b-button
                @click="submit()"
                pill
                style="background: #73dbac; color: #000; border: none"
                >Submit</b-button
              >
              3/3
            </b-modal>
            <br />
            <br />
            <h4 style="color: #fff">
              All you need is a smartphone - Take this survey & start earning
              ₦30,000 to ₦50,000 monthly
            </h4>
          </div>
        </div>
        <div class="col-lg-6"></div>
      </div>
    </div>
    <div id="about" class="container-lg" style="text-align: left">
      <br />
      <hr />
      <h1>About this program</h1>
      <p>
        EasyFinance SME Digital Finance Associate is a program designed to
        assist micro, small, and medium-sized enterprises (SMEs) in gaining
        access to essential financial services for long-term growth. The program
        will leverage EasyFinance independent sales model (and youth development
        initiative) to build a strong SME ecosystem/network in Nigeria and
        support them on their journey to sustainable growth.
      </p>

      <p>
        The program is designed for digitally aware youths with keen interest in
        making a difference in their lives and communities. Participants will
        receive a certificate of completion at the end of the training program
        and will have gained skills to effectively take on digital selling
        opportunities. They will also learn how to set up and run their own SME
        service/support agency focused on providing essential financial services
        to small businesses. Participants who meet the criteria will receive
        ongoing support after the program is completed.
      </p>
      <p>This program will:</p>
      <ul>
        <li>
          Educate you on the importance of digital and financial inclusion
        </li>
        <li>
          Allow you to build a successful business by leveraging tried-and-true
          models.
        </li>
        <li>
          Allow Africans to participate in a large and growing online and
          fintech boom
        </li>
        <li>Assist businesses in accessing innovative financial services</li>
      </ul>
      <br />
      <h1>Best in Industry Training</h1>
      <p>
        The 45-hour training program (over the course of one week) will be led
        by experienced facilitators. Participants will be given a robust set of
        tools that will prepare them to start their own business, work for a SME
        support agency, join an innovative fintech company, or work for a large
        organization in a role related to digital and financial inclusion.
      </p>
      <p>
        Follow up training for additional business tools and earning
        certifications allow you to earn up to #50,000 monthly
      </p>
      <ul>
        <li>How to run facebook ads</li>
        <li>SMS marketing</li>
        <li>Email marketing</li>
      </ul>
      <br />
      <h1>Selection Criteria</h1>
      <p>To qualify for the program, applicants must:</p>
      <ul>
        <li>
          Have obtained (at least) a diploma from an accredited tertiary
          institution
        </li>
        <li>Early-in-career</li>
        <li>People person and customer centric</li>
        <li>
          Commit to the terms and condition of the BMI program (primarily commit
          to complete the program)
        </li>
        <li>Be at least 18 years of age</li>
        <li>Submit a CV showing business experience</li>
        <li>
          Be familiar with word processing and spreadsheet applications,
          presentation tools, internet and mobile technology, and social media
          tools
        </li>
        <li>Social impact oriented</li>
        <li>Looking for mentorship and career growth</li>
      </ul>
      <br />
      <h1>
        What are the benefits of the SME Digital Finance Associate program?
      </h1>
      <p>
        Successful participants of the program will acquire the following
        skills:
      </p>
      <ul>
        <li>
          Ability to build and manage a digital business independently or with
          staff
        </li>
        <li>
          Ability to assess SMEs’ digital and financial needs and proffer
          appropriate solutions
        </li>
        <li>Fintech (Easyfinance) products and services</li>
        <li>
          Ability to effectively pitch online and financial products to SMEs
        </li>
      </ul>
      <br />
      <h1>Resources required by candidates:</h1>
      <p>
        Candidates will be required to have an internet-enabled device due to
        the practical nature of the program, which will be useful during classes
        and when engaging SMEs.
      </p>
      <br />
      <h1>Certificate</h1>
      <p>
        Program certificates will be issued to successful program participants.
        To receive the certificate, participants must:
      </p>
      <ul>
        <li>
          Attend the training in full and complete all course requirements
        </li>
        <li>Achieve minimum number of referrals</li>
        <li>
          Satisfactorily complete customer onboarding and activation process,
          including presentations on key learnings
        </li>
      </ul>
      <h1>Participant benefits:</h1>
      <p>
        Individuals that obtain the BMI program certificate will become eligible
        for ongoing support of their business by EasyFinance. Support provided
        may include:
      </p>
      <ul>
        <li>Funding (loan)</li>
        <li>Workspace</li>
        <li>Devices (financing)</li>
        <li>Internet access</li>
        <li>Marketing support</li>
        <li>Business advisory and mentorship</li>
        <li>Ongoing education and access to free training material</li>
      </ul>
      <hr />
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "Home",
  data() {
    return {
      size_error: null,
      firstname: null,
      lastname: null,
      email: null,
      phone: null,
      gender: null,
      genderOptions: {
        male: "Male",
        female: "Female",
      },
      work: null,
      workOptions: {
        "0-1 year": "0-1 year",
        "2-3 years": "2-3 years",
        "4-5 years": "4-5 years",
        Other: "Other",
      },
      education: null,
      eduOptions: {
        SSCE: "SSCE",
        OND: "OND",
        HND: "HND",
        BSc: "BSc",
        Other: "Other",
      },
      dob: null,
      state: null,
      stateOptions: {
        1: "Abia",
        2: "Abuja",
        3: "Adamawa",
        4: "Akwa Ibom",
        5: "Anambra",
        6: "Bauchi",
        7: "Bayelsa",
        8: "Benue",
        9: "Borno",
        10: "Cross River",
        11: "Delta",
        12: "Ebonyi",
        13: "Edo",
        14: "Ekiti",
        15: "Enugu",
        16: "Gombe",
        17: "Imo",
        18: "Jigawa",
        19: "Kaduna",
        20: "Kano",
        21: "Katsina",
        22: "Kebbi",
        23: "Kogi",
        24: "Kwara",
        25: "Lagos",
        26: "Nassarawa",
        27: "Niger",
        28: "Ogun",
        29: "Ondo",
        30: "Osun",
        31: "Oyo",
        32: "Plateau",
        33: "Rivers",
        34: "Sokoto",
        35: "Taraba",
        36: "Yobe",
        37: "Zamfara",
      },
      devices: [],
      accessOptions: {
        "1-2 hours": "1-2 hours",
        "2-4 hours": "2-4 hours",
        "5 hours and above": "5 hours and above",
      },
      access: null,
      businessOptions: {
        Yes: "Yes",
        No: "No",
      },
      commit: null,
      commitOptions: {
        Yes: "Yes",
        No: "No",
      },
      why: null,
      hear: null,
      address: null,
      id_doc: null,
      bizType: null,
      income: null,
      business: null,
      locationOptions: {
        Yes: "Yes",
        No: "No",
      },
      location: null,
    };
  },
  methods: {
    hide1() {
      this.$refs["modal-1"].hide();
    },
    hide2() {
      this.$refs["modal-2"].hide();
    },
    hide3() {
      this.$refs["modal-3"].hide();
    },
    dateDisabled(ymd, date) {
      // Disable weekends (Sunday = `0`, Saturday = `6`) and
      // disable days that fall on the 13th of the month
      const weekday = date.getDay();
      const day = date.getDate();
      // Return `true` if the date should be disabled
      return weekday === 0 || weekday === 6 || day === 13;
    },
    async submit() {
      if (this.size_error) {
        return;
      }
      const file = document.getElementById("photo").files[0];

      const reader = new FileReader();

      let that = this;
      let rawImg;
      reader.onloadend = () => {
        rawImg = reader.result;
        that.id_doc = rawImg;
      };
      reader.readAsDataURL(file);
      let data = {
        firstname: this.firstname,
        lastname: this.lastname,
        email: this.email,
        phone: this.phone,
        gender: this.gender,
        date_of_birth: this.dob,
        applicant_state: this.state,
        workExperience: this.work,
        education: this.education,
        applicant_address: this.address,
        commitToSelling: this.commit,
        devices: this.devices,
        electricityAndPhones: this.access,
        why: this.why,
        referralSouce: this.hear,
        application_date: new Date(),
        id_doc: this.id_doc,
        owns_business: this.business,
        business_type: this.bizType,
        income: this.income,
        has_location: this.location,
      };

      try {
        axios.post("http://localhost:3000/applications", data);
      } catch (error) {
        console.error(error.message);
      }
      this.hide3();
    },
    imageToURL() {
      const file = document.getElementById("photo").files[0];

      if (file.size > 100000) {
        this.size_error = "Image is too big. Choose an image less than 100kb";
        return;
      } else {
        this.size_error = null;
      }

      const reader = new FileReader();

      let that = this;
      let rawImg;
      reader.onloadend = () => {
        rawImg = reader.result;
        that.id_doc = rawImg;
      };
      reader.readAsDataURL(file);
    },
  },
};
</script>

<style scoped></style>

<template>
  <div class="container-lg" style="text-align: left">
    <br />
    <hr />
    <h1>About this program</h1>
    <p>
      EasyFinance SME Digital Finance Associate is a program designed to assist
      micro, small, and medium-sized enterprises (SMEs) in gaining access to
      essential financial services for long-term growth. The program will
      leverage EasyFinance independent sales model (and youth development
      initiative) to build a strong SME ecosystem/network in Nigeria and support
      them on their journey to sustainable growth.
    </p>

    <p>
      The program is designed for digitally aware youths with keen interest in
      making a difference in their lives and communities. Participants will
      receive a certificate of completion at the end of the training program and
      will have gained skills to effectively take on digital selling
      opportunities. They will also learn how to set up and run their own SME
      service/support agency focused on providing essential financial services
      to small businesses. Participants who meet the criteria will receive
      ongoing support after the program is completed.
    </p>
    <p>This program will:</p>
    <ul>
      <li>Educate you on the importance of digital and financial inclusion</li>
      <li>
        Allow you to build a successful business by leveraging tried-and-true
        models.
      </li>
      <li>
        Allow Africans to participate in a large and growing online and fintech
        boom
      </li>
      <li>Assist businesses in accessing innovative financial services</li>
    </ul>
    <br />
    <h1>Best in Industry Training</h1>
    <p>
      The 45-hour training program (over the course of one week) will be led by
      experienced facilitators. Participants will be given a robust set of tools
      that will prepare them to start their own business, work for a SME support
      agency, join an innovative fintech company, or work for a large
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
    <h1>What are the benefits of the SME Digital Finance Associate program?</h1>
    <p>
      Successful participants of the program will acquire the following skills:
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
      Candidates will be required to have an internet-enabled device due to the
      practical nature of the program, which will be useful during classes and
      when engaging SMEs.
    </p>
    <br />
    <h1>Certificate</h1>
    <p>
      Program certificates will be issued to successful program participants. To
      receive the certificate, participants must:
    </p>
    <ul>
      <li>Attend the training in full and complete all course requirements</li>
      <li>Achieve minimum number of referrals</li>
      <li>
        Satisfactorily complete customer onboarding and activation process,
        including presentations on key learnings
      </li>
    </ul>
    <h1>Participant benefits:</h1>
    <p>
      Individuals that obtain the BMI program certificate will become eligible
      for ongoing support of their business by EasyFinance. Support provided may
      include:
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
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {};
  },
  methods: {
    async test() {
      //const config = { responseType: 'blob' };
      axios
        .get("http://localhost:3000/applications" /* , config */)
        .then((res) => {
          console.log(res.data[3].id_doc.data);
        });
    },
  },
  mounted() {
    this.test();
  },
};
</script>

<template>
  <div class="container">
    <div class="row">
      <div class="col">
        <b-nav>
          <b-nav-item>About Me</b-nav-item>
          <b-nav-item>Projects</b-nav-item>
          <b-nav-item>Contact Me</b-nav-item>
        </b-nav>
      </div>
    </div>
    <div class="row">
      <div class="col">
        <b-jumbotron header="Neil Edwards" lead="Full Stack Software Developer, New York City"></b-jumbotron>
      </div>
    </div>
    <div class="row">
      <div class="col">
        <h1>About Me</h1>
        <ul>
          <li>Started as a Software Developer {{getDate()}}</li>
          <li>Proficient in .NET, Javascript, SQL, Ruby</li>
          <li>Full Stack knowledge including:</li>
          <ul>
            <li>Vuejs, React, Bootstrap</li>
            <li>NodeJS, Ruby on Rails</li>
            <li>(No)Sql databases (SQL Server, Oracle, Postgres, DynamoDB)</li>
            <li>Many AWS services, Terraform, Ansible</li>
          </ul>
        </ul>
      </div>
    </div>
    <div class="row">
      <div class="col">
        <h2>Employment History</h2>
        <ul>
          <li>Major Investment Bank 2005-Present</li>
          <ul>
            <li>Greenfield Realtime Payments system integrated into legacy codebase</li>
            <li>Designed/Built all new interfaces into core banking system</li>
          </ul>
        </ul>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';
import moment, { Moment } from 'moment';

@Component
export default class HelloWorld extends Vue {
  @Prop() private msg!: string;

  private getDate() {
    return moment('20050926', 'YYYYMMDD').fromNow();
  }
}
</script>

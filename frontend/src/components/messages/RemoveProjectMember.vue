<!--
SPDX-FileCopyrightText: 2020 SAP SE or an SAP affiliate company and Gardener contributors

SPDX-License-Identifier: Apache-2.0
-->

<template>
  <div>
    <template v-if="namespace && memberName">
      Do you want to remove the service account <i>{{memberName}}</i> of namespace <i>{{namespace}}</i>
      from the project <i>{{projectName}}</i>?
    </template>
    <template v-else-if="memberName">
      Do you want to remove the user <i>{{memberName}}</i> from the project <i>{{projectName}}</i>?
    </template>
    <template v-else>
      Do you want to remove <span class="error--text font-weight-bold">yourself</span>
      from the project <i>{{projectName}}</i>?
    </template>
  </div>
</template>

<script>
export default {
  props: {
    projectName: {
      type: String,
      required: true
    },
    memberName: String,
    namespace: String
  }
}
</script>

<template>
    <v-container>
        <v-col align="center">
            <PricingSelector v-on:selectType="onSelectType"/>

            <div class="cards-grid">
                <PricingCard v-bind:data="data[type][0]"/>
                <PricingCard v-bind:data="data[type][1]"/>
                <PricingCard v-bind:data="data[type][2]"/>
                <PricingCard v-bind:data="data[type][3]"/>
            </div>

        </v-col>
    </v-container>
</template>


<script>
    export default {
        data() {
            return {
                type:0,
                data: 
                [
                    [  
                        {
                            title: 'Starter',
                            price: 'Free',
                            time:  'Forever',
                            features: [
                                "Figma editor",
                                "3 collaborative design files",
                                "Unlimited personal drafts",
                                "Basic file inspection",
                            ],
                        },
                        
                        {
                            title: 'Professional',
                            price: '$12/mo',
                            features: [
                                "Unlimited Figma files",
                                "Team libraries",
                                "Advanced prototyping",
                                "Advanced codegen",
                                "Annotations and status",
                                "Unlimited version history",
                                "Shared and private projects",
                             ],
                        
                        },

                        {
                            title: 'Organization',
                            price: '$45/mo',
                            features: [
                                "Org-wide libraries",
                                "Design system analytics",
                                "Branching and merging",
                                "Private plugins",
                                "Centralized file management",
                                "Unified admin and billing",
                                "Single sign-on",
                            ],
                        },

                        {
                            title: 'Enterprise',
                            price: '$75/mo',
                            features: [
                                "Advanced theming with 40 modes",
                                "REST API for variables",
                                "Design system defaults by workspace",
                                "Syncing workflows via REST API",
                                "Dedicated workspaces",
                                "Guest access controls",
                                "Role setting via SCIM",
                                "Idle session timeout",
                                "Advanced link sharing controls"
                            ],
                        }
                    ],
                    [
                        {
                            title: 'Starter',
                            price: 'Free',
                            time:  'Forever',
                            features: [
                                "Figma editor",
                                "3 collaborative design files",
                                "Unlimited personal drafts",
                                "Basic file inspection",
                            ],
                        },
                        {
                            title: 'Professional',
                            price: '$3/mo*',
                            features: [
                                "Unlimited FigJam files",
                                "Open sessions",
                                "Sharing permissions",
                                "Team libraries",
                                "Audio conversations",
                                "Voting",
                            ],
                        },

                        {
                            title: 'Organization',
                            price: '$5/mo',
                            features: [
                                "Org-wide libraries",
                                "Centralized content management",
                                "Custom templates",
                                "Custom color palettes",
                                "Unified admin and billing",
                                "Private plugins and widgets",
                                "Single sign-on",
                            ],
                        },

                        {
                            title: 'Enterprise',
                            price: '$5/mo',
                            features: [
                            "Dedicated workspaces",
                            "Advanced design systems",
                            "Guest access controls",
                            "Role setting via SCIM",
                            "Idle session timeout",
                            "Enforced password links",
                            "Network access restrictions",
                            "Onboarding and account support",
                            "Expiring public links",
                            ],
                        },

                        
                    ]
                ],
            }
        },
        methods: {
            onSelectType(type) {
                this.type = type;

            }
        }
    }
</script>

<style scoped>
    .cards-grid {
    display: grid;
    grid-template-columns: repeat(4, minmax(0px, 1fr));
    gap: 12px;
    margin: 12px auto 32px;
    }
</style>
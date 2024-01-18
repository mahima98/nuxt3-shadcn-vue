<template>
  <div
    class="flex flex-col *:flex *:items-center *:gap-2 items-center gap-4 justify-center w-full h-screen"
  >
    <h1 class="text-lg font-bold">
      Building a page using Nuxt3 with Shadcn-vue
    </h1>
    <h2 class="bg-teal-100 px-1 my-4">Some components examples</h2>
    <div>Button: <Button>Shadcn</Button></div>
    <div>
      Avatar:
      <Avatar>
        <AvatarImage src="https://github.com/radix-vue.png" alt="@radix-vue" />
        <AvatarFallback>CN</AvatarFallback>
      </Avatar>
    </div>
    <div>
      Combobox:
      <Combobox />
    </div>
    <div>
      formTemplate:
      <FormTemplate />
    </div>
    <div>
      toast
      <Button
        variant="outline"
        @click="
          () => {
            toast({
              title: 'Scheduled: Catch up',
              description: 'Friday, February 10, 2023 at 5:57 PM',
            });
          }
        "
      >
        Add to calander
      </Button>
    </div>
  </div>
</template>
<script setup lang="ts">
// import { Calendar } from "@/components/ui/calendar";
import { Avatar, AvatarFallback, AvatarImage } from "@/components/ui/avatar";
import { Button } from "@/components/ui/button";
import { useToast } from "@/components/ui/toast/use-toast";

const { toast } = useToast();
</script>
